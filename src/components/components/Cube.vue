<template>
  <div class="cube__container border">
    <!-- <div class="cube border2" @mouseover="mouseover($event)" 
    data-tilt-scale="0" 
          data-tilt-speed="1000" 
         data-tilt-max="50" > -->
    <div class="cube border2">
      <div class="front" @mouseover="mouseover($event)" data-tilt-axis="y" data-tilt-glare data-tilt-max-glare="0.8" data-tilt>
        <div class="inner-front">
          <h1>juanrod</h1>
        </div>
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
export default {
  name:'Cube',
  methods:{
    mouseover (e) {
      console.log('e.target:',e.target.parentElement)
      // let className = e.target.parentElement.classList[0]
      let className = e.target.classList[0]
      const element = document.querySelector('.'+className);
        VanillaTilt.init(element);
    }
   }
}
</script>

<style>

</style>
