<template>
  <div class="cube__container ">
  
    <div class="cube ">
      <div class="front" @mouseover="mouseover($event)" data-tilt-axis="y" data-tilt>
      <!-- <div class="front" @mouseover="mouseover($event)" data-tilt-axis="y" data-tilt-glare data-tilt-max-glare="0.8" data-tilt> -->
        <!-- <div class="inner-front">
          <h1>juanrod</h1>
        </div> -->
        <the-block></the-block>
      </div>
      <div class="back"></div>
      <div class="left"></div>
      <div class="right"></div>
      <div class="top"></div>
      <div class="bottom"></div>
    </div>
  </div>
</template>

<script>
import TheBlock from './Block.vue'
export default {
  name:'Cube',
  components: { TheBlock },
  methods:{
    mouseover (e) {
      console.log('e.target:',e.target.parentElement)
      // let className = e.target.parentElement.classList[0]
      // let className = e.target.classList[0]
      // const element = document.querySelector('.'+className);
      //   VanillaTilt.init(element);
    }
   }
}
</script>

<style>

</style>
