<script>
	import quizData from '$lib/quiz.json';
	import animeMeta from '$lib/anime.json';
	import AnimeIcon from './AnimeIcon.svelte';
	let questions = quizData;

	let quizState = [];
	let selectedOptions = [];
	let currentQuestion = 0;
	let scores = {};
	let showResult = false;
	let resultAnime = null;
	let resultAnimeIcon = null;

	function selectOption(option) {
		for (const anime in option.scores) {
			scores[anime] = (scores[anime] || 0) + option.scores[anime];
		}
		quizState.push(option);
		selectedOptions.push(option.oid);

		if (currentQuestion < questions.length - 1) {
			currentQuestion++;
		} else {
			calculateResult();
			showResult = true;
		}
	}

	function calculateResult() {
		if (
			JSON.stringify(selectedOptions) ===
			JSON.stringify(['1D', '2B', '3A', '4A', '5C', '6A', '7A', '8C', '9C', '10D'])
		) {
			resultAnime = 'frieren';
		} else {
			let maxScore = Math.max(...Object.values(scores));
			let topAnimes = Object.keys(scores).filter((a) => scores[a] === maxScore);
			resultAnime = topAnimes[Math.floor(Math.random() * topAnimes.length)];
		}
		resultAnimeIcon = animeMeta.find((a) => a.slug === resultAnime).icon;
	}
</script>

{#if !showResult}
	<section class="quiz">
		<div class="quiz-card">
			<h2>{currentQuestion + 1}. {questions[currentQuestion].text}</h2>
			<div class="options">
				{#each questions[currentQuestion].options as option}
					<button class="options-btn" onclick={() => selectOption(option)}>{option.text}</button>
				{/each}
			</div>
		</div>
	</section>
{:else}
	<section class="quiz-result">
		<div class="result-card">
			<h2>Ma-Chan has found your match!</h2>
			<AnimeIcon icon={resultAnimeIcon} />
			<p>Show this at the CAC booth to get your anime recommendation :)</p>
		</div>
	</section>
{/if}

<style>
	.quiz,
	.quiz-result {
		display: flex;
		align-items: center;
		justify-content: center;
		padding: 10px;
		color: white;
	}

	.quiz-card {
		max-width: 600px;
		text-align: center;
	}

	.result-card {
		max-width: 600px;
		text-align: center;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.quiz-card h2,
	.result-card h2 {
		font-size: 1.6rem;
	}

	.options {
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: 1fr 1fr;
		gap: 5px;
	}

	.options-btn {
		display: block;
		width: 100%;
		margin: 6px 0;
		padding: 10px;
		font-size: 1rem;
		border: none;
		border-radius: 10px;
		background-color: #ffbb22;
		color: black;
		cursor: pointer;
		transition: background 0.2s ease;
	}

	.options-btn:hover,
	.options-btn:active,
	.options-btn:focus-visible {
		background-color: #ca3131;
		color: white;
	}

	@media (max-width: 600px) {
		.options {
			grid-template-rows: repeat(4, 1fr);
			grid-template-columns: 1fr;
		}
	}
</style>
