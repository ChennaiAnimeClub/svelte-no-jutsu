<a
	class="linktree-btn"
	aria-label="open Linktree"
	href="https://linktr.ee/chennai_anime_club"
	target="_blank"
>
	<span class="tabler--brand-linktree"></span>
</a>

<style>
	.tabler--brand-linktree {
		display: inline-block;
		width: 24px;
		height: 24px;
		--svg: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath fill='none' stroke='%23000' stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M4 10h16M6.5 4.5l11 11m-11 0l11-11M12 10V2m0 13v7'/%3E%3C/svg%3E");
		background-color: currentColor;
		-webkit-mask-image: var(--svg);
		mask-image: var(--svg);
		-webkit-mask-repeat: no-repeat;
		mask-repeat: no-repeat;
		-webkit-mask-size: 100% 100%;
		mask-size: 100% 100%;
	}

	.linktree-btn {
		display: inline-flex;
		align-items: center;
		gap: 0.5rem;
		font-size: 1rem;
		padding: 0.5rem 1rem;
		cursor: pointer;
		background: var(--nav-bg);
		color: var(--nav-tx);
		border-style: solid;
		border-color: var(--nav-tx);
		border-width: 1px;
		transition:
			background 0.3s ease,
			transform 0.2s ease;
	}

	.linktree-btn:hover {
		transform: scale(1.05);
	}
</style>
