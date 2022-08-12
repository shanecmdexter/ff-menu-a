<script>
  export let value = 'Menu Item'
  export let onClick = () => console.log('clicked: ', value)
  export let isLink = false
  export let disabled = false
  export let fontSize = "normal"
</script>

<div 
  class="menu-item" 
  data-is-link={isLink}
  on:click={onClick}
  data-disabled={disabled}
  data-size={fontSize}
  >
  <p>{value}</p>
</div>

<style>
  .menu-item{
    font-weight: normal;
    color: var(--off-white);
    line-height: 1; 
  }

  [data-is-link="true"] {
    cursor: pointer;
  }

  [data-is-link="true"]:not([data-disabled="true"]):hover {
    color: goldenrod;
  }
   
  [data-disabled="true"] {
    opacity: 0.5;
  }


  [data-size="normal"] {
    font-size: 1.5em;
  }
  [data-size="small"] {
    font-size: 0.9em;
  }
  [data-size="large"] {
    font-size: 2em;
  }
</style>