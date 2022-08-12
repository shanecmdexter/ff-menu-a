<script>
	import '@/styles'
</script>

<main>
	<slot />
</main>

<style>
	main {
		background-color: var(--off-black);
		height: 100vh;
		width: 100vw;
		position: absolute;
		top: 0;
		bottom: 0;
		left: 0;
		right: 0;
	}
</style>