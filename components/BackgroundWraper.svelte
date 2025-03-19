<script>
	import BackgroundSvg from "$lib/components/BackgroundSVG.svelte";
</script>

<div class="background-wrapper">
	<BackgroundSvg />
</div>

<style>
	.background-wrapper {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		width: 100vw;
		height: 100vh;
		overflow: hidden;
		z-index: 2;
	}
</style>
