<script>
  import Box from '@/components/ui/box.svelte'
  import Character from '@/components/elements/character.svelte'
  import {cloud, tifa, squall, tidus} from '@/data/avatars.js'
  
  const characters = [

    {
      name: 'Squall',
      avatar: squall,
      lv: 40,
      hp: {
        current: 90,
        max: 100,
      },
      mp: {
        current: 44,
        max: 100,
      },
      exp: {
        current: 33,
        required: 100,
      },
      limit: {
        current: 13,
        required: 100,
        lv: 1,
      },
    },
    {
      name: 'Cloud',
      avatar: cloud,
      lv: 50,
      hp: {
        current: 90,
        max: 100,
      },
      mp: {
        current: 44,
        max: 100,
      },
      exp: {
        current: 2,
        required: 100,
      },
      limit: {
        current: 13,
        required: 100,
        lv: 1,
      },
    },
    {
      name: 'Tifa', 
      avatar: tifa,
      lv: 60,
      hp: {
        current: 50,
        max: 100,
      },
      mp: {
        current: 44,
        max: 100,
      },
      exp: {
        current: 33,
        required: 100,
      },
      limit: {
        current: 13,
        required: 100,
        lv: 1,
      },
    }

  ]
</script>

<div class="character-list">
  <Box>

    <ul>
      {#each characters as char}
        <Character 
          character={ char }
        />
      {/each}
    </ul>

  </Box>
</div>

<style>
  .character-list {
    height: 100%;
    width: 100%;
  }

  ul {
    height: 100%; 
    padding: 30px 60px ;
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 20px; 
    align-content: center;
    align-items:  center;
  }
</style>
