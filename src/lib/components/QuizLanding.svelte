<script>
	let { startQuiz } = $props();
</script>

<div class="landing">
	<div class="card" in:fade>
		<h1>Ma-Chan, The Matchmaker</h1>
		<p>Let full-time mascot and part-time matchmaker Ma-Chan find the perfect anime for you ..</p>
		<button onclick={startQuiz} aria-label="Find Your Match"> Find Your Match </button>
	</div>
</div>

<style>
	.landing {
		display: flex;
		align-items: center;
		justify-content: center;
		padding: 20px;
	}

	.card {
		max-width: 600px;
		text-align: center;
		padding: 40px;
	}

	.card h1 {
		font-size: 2rem;
		font-weight: 700;
		margin-bottom: 16px;
	}

	.card p {
		font-size: 1.1rem;
		margin-bottom: 24px;
	}

	.card button {
		padding: 12px 24px;
		font-size: 1rem;
		font-weight: 600;
		border: none;
		border-radius: 4rem;
		background-color: #610404;
		color: white;
		cursor: pointer;
		transition:
			transform 0.15s ease,
			box-shadow 0.15s ease;
	}

	.card button:hover {
		background-color: #ca3131;
	}

	.card button:active {
		transform: scale(0.96);
	}
</style>
