<script>
	export let width = '100%'
	export let height = '100%'
	export let backgroundColor = 'var(--off-white);'

	$: containerStyle = `
		height: ${height};
		width: ${width};
	`
</script>

<div class="box" style={containerStyle}>
	<slot />
</div>

<style>
	.box {
		background: var(--dark-gray);
		border: solid thin lightgray;
		padding: 10px;
		border-radius: 4px;
	}
</style>
