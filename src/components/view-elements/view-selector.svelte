<script>
  import Box from '@/components/ui/box.svelte'
  import Text from '@/components/ui/text.svelte'
  import {goto} from '$app/navigation'

  function goToView(path){
    goto(path)
  }
  
  const views = [
    {name: 'Item', path: '/item', description: 'View items', onClick: goToView},
    {name: 'Magic', path: '/magic', description: 'View magic', onClick: goToView},
    {name: 'Materia', path: '/materia', description: 'View materia', onClick: goToView},
    {name: 'Equip', path: '/equip', description: 'View equipment', onClick: goToView},
    {name: 'Status', path: '/status', description: 'View character status', onClick: goToView},
    {name: 'Order', path: '/order', description: 'Change character order', onClick: goToView},
    {name: 'Limit', path: '/limit', description: 'View and change character limit break', onClick: goToView},
    {name: 'Order', path: '/order', description: 'Change character order', onClick: goToView},
    {name: 'Config', path: '/config', description: 'Adjust game configuration', onClick: goToView},
    {name: 'PHS', path: '/phs', description: 'Change party', onClick: goToView, hide: true},
    {name: 'Save', path: '/save', description: 'Save your game', onClick: goToView, disabled: true},
  ]
</script>

<div class="view-selector-list"> 
  <Box>
    <ul>
      {#each views as view}

        <li class="flex">
          {#if view.hide}
            <div class="is-hidden"></div>
          {:else}
            <Text
              isLink={true}
              value={view.name} 
              onClick={() => view.onClick(view.path)}
              disabled={view.disabled}
              fontSize="large" 
            />
          {/if}
        </li>

      {/each}
    </ul>
  </Box>
</div>

<style>
  .view-selector-list {
    height: auto;
    width: 300px;
    position: absolute;
    top: 40px;
    right: 20px;
  }

  ul {
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 15px;
    margin: 0;
    padding: 10px;
  }

  li {
    width: 100%;
    height: 40px;
    justify-content: flex-start;
  }

  .is-hidden {
    height: 50px;
  }

</style>
