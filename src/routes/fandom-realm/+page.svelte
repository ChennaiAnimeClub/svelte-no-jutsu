<script>
	import AnimeIndiaBanner from '$lib/components/AnimeIndiaBanner.svelte';
	import Quiz from '$lib/components/Quiz.svelte';
	import QuizLanding from '$lib/components/QuizLanding.svelte';
	import { fade, fly } from 'svelte/transition';

	let started = false;

	function startQuiz() {
		started = true;
	}
</script>

<div class="landing-container">
	<AnimeIndiaBanner />
	<div class="quiz-container">
		{#if !started}
			<QuizLanding {startQuiz} />
		{:else}
			<Quiz />
		{/if}
	</div>
</div>

<style>
	.landing-container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 0.8rem;
		font-family: 'Anek Tamil';
		padding-bottom: 1rem;
	}

	.quiz-container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		background-color: #885599;
		color: black;
		width: 90vw;
		height: fit-content;
		border-radius: 1rem;
	}

	@media (max-width: 600px) {
		.quiz-container {
			min-height: 400px;
		}
	}
</style>
