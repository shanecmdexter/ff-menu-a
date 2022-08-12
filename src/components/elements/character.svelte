<script>
  import Avatar from "@/components/ui/character-avatar.svelte";
  import CharacterInfo from "@/components/elements/character-info.svelte";
  import {defaultImage} from '@/data/avatars.js'

  export let character = {
      name: 'Default Char',
      avatar: defaultImage,
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
        toNext: 100,
        lv: 1,
      },
  }
</script>

<div class="character">
  <!-- image -->
  <Avatar 
    image={character.avatar}
  />
  <!-- info -->
  <CharacterInfo
    lvl={character.lvl}
    name={character.name}
    maxHp={character.hp.max}
    currentHp={character.hp.current}

    maxMp={character.mp.max}
    currentMp={character.mp.current}

    currentExp={character.exp.current}
    requiredExp={character.exp.required}

    limitLevel={character.limit.lv}
    currentLimitExp={character.limit.current}
    requiredLimitExp={character.limit.toNext}
  />
  
  <!-- limit/exp -->

</div>


<style>
  .character {
    display: grid; 
    grid-template-columns: 250px 1fr;
    grid-gap: 40px;
    align-items: center;
  }
</style>