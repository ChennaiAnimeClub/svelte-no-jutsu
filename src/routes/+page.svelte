<script>
	import AnimeIndiaBanner from '$lib/components/AnimeIndiaBanner.svelte';
	import WelcomeSection from '$lib/components/WelcomeSection.svelte';
</script>

<div class="homepage-container">
	<AnimeIndiaBanner />
	<WelcomeSection />
</div>

<style>
	.homepage-container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 1rem;
	}
</style>
