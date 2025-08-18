<script>
	let questions = [
		{
			qid: '1',
			text: 'Pick your ideal weekend activity',
			options: [
				{ oid: '1A', text: 'Binge an anime marathon', scores: { aot: 2 } },
				{ oid: '1B', text: 'Chill at the beach', scores: { nagatoro: 2 } },
				{ oid: '1C', text: 'Read manga in a café', scores: { fruitsbasket: 1 } },
				{ oid: '1D', text: 'Go for a jog', scores: { haikyuu: 2 } }
			]
		},
		{
			qid: '2',
			text: 'Which snack are you grabbing?',
			options: [
				{ oid: '2A', text: 'Ramen', scores: { naruto: 2 } },
				{ oid: '2B', text: 'Onigiri', scores: { gintama: 1 } },
				{ oid: '2C', text: 'Ice cream', scores: { ouran: 2 } },
				{ oid: '2D', text: 'Energy drink', scores: { jojo: 2 } }
			]
		}
	];

	let quizState = [];
	let currentQuestion = 0;
	let scores = {};
	let showResult = false;
	let resultAnime = null;

	function selectOption(option) {
		for (const anime in option.scores) {
			scores[anime] = (scores[anime] || 0) + option.scores[anime];
		}
		quizState.push(option);

		if (currentQuestion < questions.length - 1) {
			currentQuestion++;
		} else {
			calculateResult();
			showResult = true;
		}
	}

	function calculateResult() {
		console.log(quizState);
		let maxScore = Math.max(...Object.values(scores));
		let topAnimes = Object.keys(scores).filter((a) => scores[a] === maxScore);
		resultAnime = topAnimes[Math.floor(Math.random() * topAnimes.length)];
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
			<p><strong>{resultAnime}</strong></p>
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
	}

	.quiz-card,
	.result-card {
		max-width: 600px;
		text-align: center;
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
		margin: 8px 0;
		padding: 12px;
		font-size: 1rem;
		border: none;
		border-radius: 10px;
		background-color: #885599;
		color: white;
		cursor: pointer;
		transition: background 0.2s ease;
	}

	.options-btn:hover {
		background-color: #9e66b3;
	}

	.options-btn:active {
		background-color: #ffbb22;
		color: black;
	}

	@media (max-width: 600px) {
		.options {
			grid-template-rows: repeat(4, 1fr);
			grid-template-columns: 1fr;
		}
	}
</style>
