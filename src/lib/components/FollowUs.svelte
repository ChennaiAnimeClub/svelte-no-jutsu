<section>
	<h4>Follow for Updates</h4>
	<div class="grid">
		<a
			href="https://www.instagram.com/chennai_anime_club/"
			target="_blank"
			rel="noopener"
			class="btn"
		>
			<span class="hugeicons--instagram"></span> Instagram
		</a>
		<a href="https://www.reddit.com/r/ChennaiAnimeClub/" target="_blank" rel="noopener" class="btn">
			<span class="hugeicons--reddit"></span> Reddit
		</a>
	</div>
</section>

<style>
	.grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
		gap: 1rem;
	}

	h4 {
		margin-top: 16px;
		margin-bottom: 8px;
	}

	.btn {
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 0.5rem;
		background: black;
		color: white;
		padding: 0.6rem 1rem;
		border-radius: 4px;
		text-decoration: none;
		font-weight: 600;
	}

	@media (hover: hover) and (pointer: fine) {
		.btn:hover,
		.btn:active,
		.btn:focus-visible {
			background: #ca3131;
		}
	}

	.hugeicons--instagram {
		display: inline-block;
		width: 24px;
		height: 24px;
		--svg: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cg fill='none' stroke='%23000' stroke-linecap='round' stroke-linejoin='round' stroke-width='1.5'%3E%3Cpath d='M2.5 12c0-4.478 0-6.718 1.391-8.109S7.521 2.5 12 2.5c4.478 0 6.718 0 8.109 1.391S21.5 7.521 21.5 12c0 4.478 0 6.718-1.391 8.109S16.479 21.5 12 21.5c-4.478 0-6.718 0-8.109-1.391S2.5 16.479 2.5 12'/%3E%3Cpath d='M16.5 12a4.5 4.5 0 1 1-9 0a4.5 4.5 0 0 1 9 0m1.008-5.5h-.01'/%3E%3C/g%3E%3C/svg%3E");
		background-color: currentColor;
		-webkit-mask-image: var(--svg);
		mask-image: var(--svg);
		-webkit-mask-repeat: no-repeat;
		mask-repeat: no-repeat;
		-webkit-mask-size: 100% 100%;
		mask-size: 100% 100%;
	}

	.hugeicons--reddit {
		display: inline-block;
		width: 24px;
		height: 24px;
		--svg: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cg fill='none' stroke='%23000' stroke-linecap='round' stroke-linejoin='round' stroke-width='1.5'%3E%3Cellipse cx='12' cy='15.5' rx='9' ry='6.5'/%3E%3Cpath d='M15.5 16.78A5.67 5.67 0 0 1 12 18a5.67 5.67 0 0 1-3.5-1.22'/%3E%3Ccircle cx='19' cy='4' r='2'/%3E%3Cpath d='M18 10.07A2.14 2.14 0 0 1 19.86 9c1.182 0 2.14.95 2.14 2.12c0 .817-.466 1.526-1.15 1.88M6 10.07A2.14 2.14 0 0 0 4.14 9A2.13 2.13 0 0 0 2 11.12c0 .817.466 1.526 1.15 1.88M17 4c-2.357 0-3.536 0-4.268.732S12 6.643 12 9m-2.992 4h-.009m6.009 0h-.009'/%3E%3C/g%3E%3C/svg%3E");
		background-color: currentColor;
		-webkit-mask-image: var(--svg);
		mask-image: var(--svg);
		-webkit-mask-repeat: no-repeat;
		mask-repeat: no-repeat;
		-webkit-mask-size: 100% 100%;
		mask-size: 100% 100%;
	}
</style>
