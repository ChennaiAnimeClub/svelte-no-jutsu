<script>
	import { page } from '$app/stores';

	const leftImg = 'assets/images/oto.png';
	const rightImg = 'assets/images/kanade.png';
	const logo = 'assets/images/ai-logo-dark.png';
</script>

<div class="banner">
	<img src={leftImg} alt="Left Banner" />

	<div class="center">
		<img src={logo} alt="CAC Logo" />
		{#if $page.url.pathname !== '/fandom-realm'}
			<a class="fandom-btn" href="/fandom-realm">Check out the Fandom Realm!</a>
		{/if}
	</div>

	<img src={rightImg} alt="Right Banner" />
</div>

<style>
	.banner {
		display: flex;
		justify-content: center;
		align-items: center;
		padding: 1rem 8rem;
		background-color: #885599;
	}

	.banner img {
		max-width: 10%;
	}

	.center {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		max-width: 40%;
		padding-bottom: 1rem;
		gap: 1rem;
	}

	.center img {
		max-width: 48%;
	}

	.fandom-btn {
		padding: 0.4rem 0.8rem;
		text-decoration: none;
		font-weight: bold;
		font-family: 'Anek Tamil';
		border-radius: 2.5rem;
		border-width: 0;
		cursor: pointer;
		background-color: #610404;
		color: white;
		transition: background-color 0.2s;
	}

	.fandom-btn:hover {
		background-color: #ca3131;
	}

	@media (max-width: 1024px) {
		.banner {
			padding: 0 6rem;
			gap: 2rem;
		}

		.center {
			padding-bottom: 1rem;
			gap: 1rem;
		}

		.fandom-btn {
			padding: 0.4rem 0.7rem;
			font-size: 0.8rem;
		}
	}

	@media (max-width: 768px) {
		.banner {
			padding: 0 6rem;
			gap: 2rem;
		}

		.center {
			padding-bottom: 0.8rem;
			gap: 0.8rem;
		}

		.fandom-btn {
			padding: 0.2rem 0.3rem;
			font-size: 0.6rem;
		}
	}

	@media (max-width: 600px) {
		.banner {
			padding: 0 4rem;
			gap: 4rem;
		}

		.center {
			padding-bottom: 0.3rem;
			gap: 0.5rem;
		}

		.fandom-btn {
			padding: 0.1rem 0.2rem;
			font-size: 0.6rem;
		}
	}

	@media (max-width: 480px) {
		.banner {
			padding: 0.5rem;
			gap: 4rem;
		}

		.center {
			padding-bottom: 0;
			gap: 0.3rem;
		}

		.fandom-btn {
			padding: 0.2rem;
			font-size: 0.5rem;
		}
	}
</style>
