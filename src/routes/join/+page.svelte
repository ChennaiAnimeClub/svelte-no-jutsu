<script>
	import CommunityHubs from '$lib/components/CommunityHubs.svelte';
	import FollowUs from '$lib/components/FollowUs.svelte';
	import WatchUs from '$lib/components/WatchUs.svelte';
</script>

<div class="join-container">
	<div class="join-section">
		<h1>Join Chennai Anime Club</h1>
		<CommunityHubs />
		<FollowUs />
		<WatchUs />
	</div>
</div>

<style>
	.join-container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 0.8rem;
		font-family: 'Anek Tamil';
	}

	.join-section {
		padding: 2rem;
		max-width: 1000px;
		margin: 0 auto;
	}
	h1 {
		text-align: center;
		margin-bottom: 0.5rem;
	}
</style>
