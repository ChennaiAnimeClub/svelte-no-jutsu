<script>
	let { icon } = $props();
</script>

<div class="icon-container">
	<div class="icon-clipper">
		<span class="icon" style="--svg: url('/assets/icons/{icon}.svg');"></span>
	</div>
</div>

<style>
	.icon-container {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 80px;
		height: 80px;
		background-color: white;
		border-style: solid;
		border-width: 1px;
		border-color: black;
	}

	.icon-clipper {
		height: calc(100% - 31px);
		overflow: hidden;
		display: inline-block;
	}

	.icon {
		display: inline-block;
		width: 60px;
		height: 60px;
		background-color: black;
		-webkit-mask-image: var(--svg);
		mask-image: var(--svg);
		-webkit-mask-repeat: no-repeat;
		mask-repeat: no-repeat;
		-webkit-mask-size: 100% 100%;
		mask-size: 100% 100%;
	}
</style>
