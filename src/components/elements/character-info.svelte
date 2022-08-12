<script>
  import Text from '@/components/ui/text.svelte'
  import Space from '@/components/ui/horizontal-space.svelte'
  export let lvl = 1;
  // name
  export let name = 'Character'
  // hp
  export let currentHp = 0;
  export let maxHp = 0;
  // mp
  export let currentMp = 0;
  export let maxMp = 0;
  // exp
  export let currentExp = 0;
  export let requiredExp = 0;
  // limit
  export let limitLevel = 1;
  export let currentLimitExp = 0;
  export let requiredLimitExp = 0;
</script>

<div class="info-wrapper">
  <div class="char-info">
    <Text value={name} />
    
    <div class="level flex jc-start ai-end">
      <Text value="Lv " fontSize="small" disabled={true} />
      <Space />
      <Text value={lvl} />
    </div> 

    <div class="hp flex jc-start ai-end">
      <Text value="HP" fontSize="small" disabled={true} />
      <Space />
      <Text value={`${currentHp} /${maxHp}`} />
    </div>

    <div class="mp flex jc-start ai-end">
      <Text value="MP" fontSize="small" disabled={true} />
      <Space />
      <Text value={`${currentMp} /${maxMp}`} />
    </div>

  </div>
  <div class="limit-info">
  
  </div>
</div>

<style>
  .char-info {
    display: grid;
    grid-gap: 10px;
  }
</style>