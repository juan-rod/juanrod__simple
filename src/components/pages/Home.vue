<template>
  <div class="home ">
      <!-- <div class="home__content maxW_768" 
          data-tilt-scale="1.01" 
          data-tilt-speed="100" 
          data-tilt-perspective="500" 
          @mouseover="mouseover($event)">
          <h2>juan rodriguez</h2>
      </div> -->
      <!-- <the-cube></the-cube> -->
      <the-block></the-block>
       <!-- <div class="home__content--front maxW_768 border">
          <h2>juan rodriguez</h2>
      </div>
      <div class="home__content--back maxW_768 border2">
      </div> -->
  </div>
</template>

<script>
import VanillaTilt from '../../utils/tilt.js'
import TheCube from '../components/Cube.vue'
import TheBlock from '../components/Block.vue'
export default {
  name: 'Home',
  components: { TheBlock, TheCube },
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
