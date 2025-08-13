<script>
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

<style>
	@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Libre+Baskerville:ital,wght@0,400;0,700;1,400&display=swap');

	:global {
		:root {
			/* main */
			--bg-color: white;
			--tx-color: black;
			/* navbar */
			--nav-bg: black;
			--nav-tx: white;
			--nav-br: black;
			--nav-hv: #1f51ff;
		}

		body {
			margin: 0px;
			color: var(--tx-color);
			background-color: var(--bg-color);
			transition:
				background-color 0.3s ease,
				color 0.3s ease;
		}

		.main-container {
			padding-top: 4rem;
		}
	}
</style>
