<template>
  <div class="home ">

      <!-- <the-cube></the-cube> -->
      <the-block></the-block>
      <!-- <the-book></the-book> -->

  </div>
</template>

<script>
import VanillaTilt from '../../utils/tilt.js'
import TheCube from '../components/Cube.vue'
import TheBlock from '../components/Block.vue'
import TheBook from '../components/Book.vue'
export default {
  name: 'Home',
  components: { TheBlock, TheCube, TheBook },
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
