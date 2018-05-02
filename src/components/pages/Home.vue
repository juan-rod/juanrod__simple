<template>
  <div class="home border">
      <div class="home__content maxW_768" 
          data-tilt-scale="1.01" 
          data-tilt-speed="100" 
          data-tilt-perspective="500" 
          @mouseover="mouseover($event)">
          <h2>juan rodriguez</h2>
      </div>
  </div>
</template>

<script>
import VanillaTilt from '../../utils/tilt.js'
export default {
  name: 'Home',
  methods:{
    mouseover (e) {
      let className = e.target.classList[0]
      const element = document.querySelector('.'+className);
        VanillaTilt.init(element);
    }
   }
}
</script>

<style>

</style>
