<script>
	import Footer from '$lib/components/Footer.svelte';
	import Navbar from '$lib/components/Navbar.svelte';

	let { children } = $props();
	let currentPage = $state('home');
</script>

<svelte:head>
	<title>Chennai Anime Club</title>
	<link rel="icon" href="/favicon-32x32.png" />
</svelte:head>

<Navbar />

<div class="main-container">
	{@render children?.()}
</div>

<Footer />

<style>
	@import url('https://fonts.googleapis.com/css2?family=Anek+Tamil:wght@100..800&family=Bebas+Neue&family=Libre+Baskerville:ital,wght@0,400;0,700;1,400&display=swap');

	:global {
		:root {
			/* main */
			--bg-color: #1c1c1c;
			--tx-color: white;
			/* navbar */
			--nav-bg: #1c1c1c;
			--nav-tx: white;
			--nav-br: black;
			--nav-hv: #1f51ff;
		}

		body {
			margin: 0px;
			color: var(--tx-color);
			background-color: var(--bg-color);
			min-height: 100vh;
			display: flex;
			flex-direction: column;
			transition:
				background-color 0.3s ease,
				color 0.3s ease;
		}

		.main-container {
			padding-top: 4rem;
		}
	}
</style>
