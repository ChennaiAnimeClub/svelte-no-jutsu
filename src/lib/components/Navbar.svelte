<script>
	import { page } from '$app/stores';
	import { afterNavigate } from '$app/navigation';
	import LinktreeButton from './LinktreeButton.svelte';

	let menuOpen = false;

	afterNavigate(() => {
		menuOpen = false;
	});

	function isActive(path) {
		return $page.url.pathname === path;
	}
</script>

<nav class="navbar">
	<a class="logo" href="/">
		<img src="/assets/logos/logoW.png" alt="Chennai Anime Club" />
	</a>

	<div class="nav-links desktop">
		<a class={isActive('/') ? 'nav-link active' : 'nav-link'} href="/">HOME</a>
		<a class={isActive('/about') ? 'nav-link active' : 'nav-link'} href="/about">ABOUT</a>
		<a class={isActive('/join') ? 'nav-link active' : 'nav-link'} href="/join">JOIN</a>
		<a class={isActive('/quiz') ? 'nav-link active' : 'nav-link'} href="/quiz">QUIZ</a>
	</div>

	<div class="actions">
		<LinktreeButton />
		<div
			class="hamburger mobile"
			onclick={() => (menuOpen = !menuOpen)}
			onkeydown={(event) => {
				if (event.key === 'Enter') {
					menuOpen = !menuOpen;
				}
			}}
			role="button"
			tabindex="0"
			aria-label="open navbar menu"
		>
			<span class="hugeicons--menu-01"></span>
		</div>
	</div>

	{#if menuOpen}
		<div class="nav-links mobile">
			<a class={isActive('/') ? 'nav-link active' : 'nav-link'} href="/">HOME</a>
			<a class={isActive('/about') ? 'nav-link active' : 'nav-link'} href="/about">ABOUT</a>
			<a class={isActive('/join') ? 'nav-link active' : 'nav-link'} href="/join">JOIN</a>
			<a class={isActive('/quiz') ? 'nav-link active' : 'nav-link'} href="/quiz">QUIZ</a>
		</div>
	{/if}
</nav>

<style>
	.hugeicons--menu-01 {
		display: inline-block;
		width: 24px;
		height: 24px;
		--svg: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath fill='none' stroke='%23000' stroke-linecap='round' stroke-linejoin='round' stroke-width='1.5' d='M4 5h16M4 12h16M4 19h16'/%3E%3C/svg%3E");
		background-color: currentColor;
		-webkit-mask-image: var(--svg);
		mask-image: var(--svg);
		-webkit-mask-repeat: no-repeat;
		mask-repeat: no-repeat;
		-webkit-mask-size: 100% 100%;
		mask-size: 100% 100%;
	}

	.navbar {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		z-index: 1000;
		height: 3rem;
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 0.5rem 1rem;
		background: var(--nav-bg);
		color: var(--nav-tx);
		font-family: 'Bebas Neue';
	}

	.logo {
		cursor: pointer;
		display: flex;
		align-items: center;
	}

	.logo img {
		height: 40px;
		width: auto;
	}

	.nav-links {
		display: flex;
		gap: 1.5rem;
		align-items: center;
	}

	.nav-link {
		cursor: pointer;
		text-decoration: none;
		color: inherit;
		font-weight: 500;
		transition: color 0.3s;
	}

	.active {
		border-top: 1px solid var(--nav-tx);
		border-bottom: 1px solid var(--nav-tx);
	}

	.nav-link:hover {
		border-bottom: 1px solid var(--nav-tx);
	}

	.actions {
		display: flex;
		align-items: center;
		gap: 0.5rem;
	}

	.hamburger {
		display: inline-flex;
		align-items: center;
		gap: 0.5rem;
		font-size: 1rem;
		padding: 0.5rem 1rem;
		border-style: solid;
		border-width: 1px;
		border-color: var(--nav-tx);
	}

	.desktop {
		display: flex;
	}

	.mobile {
		display: none;
	}

	@media (max-width: 600px) {
		.desktop {
			display: none;
		}
		.mobile {
			display: inline-flex;
		}
		.nav-links.mobile {
			flex-direction: column;
			align-items: flex-end;
			box-sizing: border-box;
			background: var(--nav-bg);
			padding: 0.5rem 1rem;
			gap: 0.75rem;

			position: absolute;
			top: 100%;
			left: 0;
			width: 100%;
		}
	}
</style>
