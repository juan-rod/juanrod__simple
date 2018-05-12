<template>
  <div>
    <a class="" :href="item.src" target="_blank" @mouseover="enter($event)" @mouseleave="leave($event)"><p>{{item.name}}</p></a>
    <transition name="v--slide">
      <div :class="item.name" class="portfolio__img" v-show="showImage" key="1" data-tilt-axis="y" data-tilt-glare data-tilt-max-glare="0.8" data-tilt>
        <img :src="item.img" :alt="item.name" :class="{ img__animation: showImage }">
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'PortfolioList',
  props: {
    item: Object
  },
  data () {
    return {
      showImage: false,
    }
  },
  methods: {
     enter (e) {
      this.showImage = !this.showImage
      console.log('enter:',this.showImage)
    },
    leave (e) {
      this.showImage = !this.showImage
      
      console.log('leave:',this.showImage)
    }
  }
}
</script>

<style>

</style>
