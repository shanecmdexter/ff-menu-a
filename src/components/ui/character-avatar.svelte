<script>
  import {defaultImage} from '@/data/avatars.js'
  export let image = defaultImage
</script>

<div class="image">
  <img src={image} alt="image name"/>
</div>
<style>
  .image {
    height: 250px;
    width: 250px;
    border-radius: 6px; 
    border: solid thin black; 
    overflow: hidden; 
  }

  img {
    width: 120%;
  }
</style>