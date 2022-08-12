<script>
	import Box from '../components/ui/box.svelte'
	import CharacterList from '../components/view-elements/character-list.svelte'
	import ViewSelector from '../components/view-elements/view-selector.svelte'
</script>


<div class="main-menu-view flex">
	<CharacterList />
	<ViewSelector />
</div>

<style>
	.main-menu-view {
		width: 100%;
		height: 100%;
		padding: 50px;
	}
</style>