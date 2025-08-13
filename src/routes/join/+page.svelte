<script>
	import CommunityHubs from '$lib/components/CommunityHubs.svelte';
	import FollowUs from '$lib/components/FollowUs.svelte';
	import WatchUs from '$lib/components/WatchUs.svelte';
</script>

<section class="join-container">
	<h1>Join Chennai Anime Club</h1>
	<p class="intro">Connect and share your love for anime</p>

	<CommunityHubs />
	<FollowUs />
	<WatchUs />
</section>

<style>
	.join-container {
		padding: 2rem;
		max-width: 1000px;
		margin: 0 auto;
		font-family: 'Libre Baskerville';
	}
	h1 {
		text-align: center;
		margin-bottom: 0.5rem;
	}
	.intro {
		text-align: center;
		margin-bottom: 2rem;
	}
</style>
