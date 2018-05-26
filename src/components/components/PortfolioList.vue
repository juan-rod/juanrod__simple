<template>
  <div>
    <a target="_blank" 
       @click="openImage($event)" 
       @mouseover="enter($event)" 
       @mouseleave="leave($event)">
      <p>{{item.name}}</p>
      </a>
    <transition name="v--slide">
      <div :class="item.name" class="portfolio__img" v-if="showImage" key="1" data-tilt-axis="y" data-tilt-glare data-tilt-max-glare="0.8" data-tilt>
        <img :src="item.img" :alt="item.name" :class="{ img__animation: showImage }">
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'PortfolioList',
  props: {
    item: Object,
    index: Number,
    currentImage: String,
    showImage: Boolean
  },
  data () {
    return {
      // showImage: false,
      target: null,
      count: null
    }
  },
  // computed:{
  //   showImage(index){
  //     console.log('index in showImage computed:',index)
  //   }
  // },
  methods: {
    enter (e) {
      console.log('e:',e.target.innerText)
      // console.log('wat:','.portfolio__img.'+ e.target.innerText)
      // this.count = e
      // let previousItem = document.querySelector('.portfolio__img.'+ e.target.innerText)
      // console.log('previousItem:',previousItem)
      // if(previousItem != null) {
      //   console.log('this.target:',this.target)
      //   this.target = e.target.innerText
      //   // console.log('')
      //   previousItem.style.display = 'none';
      // }

      //  if(!this.showImage) {
        // this.showImage = !this.showImage
      // }

    },
    leave (e) {
      // if(this.showImage) {
        // this.showImage = !this.showImage
      // }
      
      // console.log('leave:',this.showImage)
    },
    openImage(e){
      console.log('click:')
    }
  }
}
</script>

<style>

</style>
