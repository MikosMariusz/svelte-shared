<script>
	import BackgroundSVG from '$lib/components/BackgroundSVG.svelte';
</script>

<div class="background-wrapper">
	<BackgroundSVG />
</div>

<style>
	.background-wrapper {
		position: absolute;
		top: 0;
		left: 0;
		width: 100vw;
		height: 100vh;
		overflow: hidden;
		z-index: 100;
	}
</style>
