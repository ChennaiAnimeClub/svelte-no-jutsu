<div class="welcome-section">
	<img class="welcome-section-logo" src="/assets/logos/logoW.png" alt="Chennai Anime Club" />
	<div class="welcome-section-desc">
		<p>
			<strong style="color: #CA3131;">Vanakkam!</strong> Welcome to the gathering spot for anime lovers
			in and around Chennai.
		</p>
		<p>Join us for meet-ups, events, conventions, and movie screenings —</p>
		<p>Dive into discussions on our WhatsApp groups and Discord server.</p>
		<p>
			Whether you’re just starting your anime journey or you’re a seasoned weeb, there’s a place for
			you here.
		</p>
	</div>
	<a href="/join" class="welcome-section-join-btn">Join The Club!</a>
</div>

<style>
	.welcome-section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 2rem 0.5rem;
		width: 100%;
		font-family: 'Anek Tamil';
		gap: 2rem;
	}

	.welcome-section-logo {
		width: 500px;
	}

	.welcome-section-desc {
		display: flex;
		flex-direction: column;
		width: 60%;
		margin: 0 auto;
		text-align: center;
		gap: 0.5rem;
	}

	.welcome-section-desc p {
		margin: 0;
	}

	.welcome-section-join-btn {
		display: inline-block;
		background-color: #ffbb22;
		color: black;
		padding: 0.6rem 1.4rem;
		border-radius: 9999px;
		font-weight: 600;
		text-decoration: none;
		transition:
			transform 0.15s ease,
			background-color 0.15s ease;
		font-size: 1rem;
		white-space: nowrap;
	}

	.welcome-section-join-btn:hover {
		background-color: #ca3131;
		color: white;
		transform: translateY(-2px);
	}

	.welcome-section-join-btn:active {
		background-color: #ca3131;
		color: white;
		transform: translateY(0);
	}

	@media (max-width: 640px) {
		.welcome-section-desc {
			width: 85%;
		}
		.welcome-section-join-btn {
			padding: 0.7rem 1.4rem;
			font-size: 1rem;
		}

		.welcome-section-logo {
			width: 250px;
		}

		.welcome-section-desc p {
			font-size: 0.9rem;
		}
	}
</style>
