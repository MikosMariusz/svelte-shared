<script lang="js">
	import { onMount } from 'svelte';
	import QRCode from 'qrcode';
	import { writable } from 'svelte/store';

	let qrText = '';
	let qrCodeCanvas;
	let qrCodeVisible = writable(false);
	let resetVisible = writable(false);

	async function generateQRCode() {
		if (qrText.length > 10) {
			const canvas = document.createElement('canvas');
			await QRCode.toCanvas(canvas, qrText, { width: 200 });
			qrCodeCanvas.innerHTML = '';
			qrCodeCanvas.appendChild(canvas);
			resetVisible.set(true);
		} else {
			alert('Tekst musi mieć więcej niż 10 znaków');
		}
	}

	function resetQRCode() {
		qrText = '';
		qrCodeCanvas.innerHTML = '';
		resetVisible.set(false);
	}

	function toggleQRContainer() {
		qrCodeVisible.update((v) => !v);
	}
</script>

<div
	class="qrgenerator absolute top-2 right-2 left-2 flex w-auto flex-wrap rounded-lg bg-white p-6 text-center shadow-lg"
>
	<h1 class="mb-4 text-2xl font-bold">Generator kodów QR</h1>
	<input
		type="text"
		bind:value={qrText}
		class="mb-4 w-full rounded border p-2"
		placeholder="Wprowadź tekst do zakodowania"
	/>
	<button
		class="mt-4 w-full rounded bg-green-500 px-2 py-2 text-white transition hover:bg-green-600 disabled:cursor-not-allowed disabled:bg-gray-200"
		on:click={generateQRCode}
		disabled={qrText.length < 10}
	>
		<i class="fas fa-qrcode"></i> Generuj kod QR
	</button>
	<div bind:this={qrCodeCanvas} class="mt-4 flex justify-center"></div>
	{#if $resetVisible}
		<button
			class="mt-4 w-full rounded bg-red-500 px-2 py-2 text-white transition hover:bg-red-600"
			on:click={resetQRCode}
		>
			<i class="fas fa-refresh"></i> Resetuj
		</button>
	{/if}
</div>

<style>
	.qrgenerator {
		z-index: 3;
	}
</style>
