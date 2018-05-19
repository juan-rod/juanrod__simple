<template>
  <div class="home ">
    <!-- <the-block></the-block> -->
    <!-- <new-cube></new-cube> -->
    <the-slate></the-slate>
  </div>
</template>

<script>
import VanillaTilt from '../../utils/tilt.js'
import TheCube from '../components/Cube.vue'
import NewCube from '../components/NewCube.vue'
import TheBlock from '../components/Block.vue'
import TheSlate from '../components/Slate.vue'
export default {
  name: 'Home',
  components: { TheBlock, NewCube, TheSlate },
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
