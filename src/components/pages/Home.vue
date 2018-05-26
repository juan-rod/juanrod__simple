<template>
  <div class="home ">
    <div class="switch--left border2" v-show="showSwitchL" @click="openSlate">x</div>
      <transition name="v--slate">
        <the-slate></the-slate>
      </transition>
    <div class="switch--right border2" v-show="showSwitchR" @click="openSlate">
      <span v-show="showSwitchR">x</span>
      </div>
  </div>
</template>

<script>
import VanillaTilt from '../../utils/tilt.js'
import TheSlate from '../components/Slate.vue'
export default {
  name: 'Home',
  components: { TheSlate },
  data () {
    return {
      showSwitchL: true,
      showSwitchR: true,

    }
  },
  methods:{
    mouseover (e) {
      let className = e.target.classList[0]
      const element = document.querySelector('.'+className);
        VanillaTilt.init(element);
    },
    openSlate () {
      let openSlate = document.querySelector('.box')
          openSlate.classList.toggle('openSlate')
          this.showSwitchR = !this.showSwitchR
    }
   }
}
</script>

<style>

</style>
