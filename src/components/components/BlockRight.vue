<template>
  <div class="block__right">
    <div class="intro">
      <h1>hi.</h1>
      <p>I am a front end developer. </p>
      <p><i class="fa fa-map-marker" aria-hidden="true"></i> Austin, Texas. </p>
      <p>I enjoy creating new stuff.</p>
    </div>
      <div class="projects">
        <h2>Projects</h2>
        <div v-for="project in projects" 
             :key="project.id" 
             class="projects__list">
          <div class="projects__main--title">
            <h3>{{project.name}}</h3>
          </div>
          <div class="projects__sub">
            <div v-for="(item,index) in project.portfolio" 
                 :key="item.id" 
                 :class="(activeImage == index) ? 'active' : ''"
                 class="projects__sub--item"
                 @click="activateImage(index)">
                  <p>{{item.name}}</p>
                <transition name="v--slide">
                  <div v-if="(activeImage == index)" 
                      key="1" data-tilt-axis="y" 
                      data-tilt-glare 
                      data-tilt-max-glare="0.8" 
                      data-tilt 
                      :class="item.name" 
                      class="portfolio__img">
                    <img :src="currentImage" :alt="item.name" :class="{ img__animation: showImage }">
                  </div>
                </transition>
              <!-- <portfolio-list :item="item" :index="index" :currentImage="currentImage" :showImage="showImage"></portfolio-list> -->
            </div>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
import PortfolioList from './PortfolioList.vue'
export default {
  name: 'BlockRight',
  components : { PortfolioList },
  data () {
    return {
      projects:[
        {
          name: 'personal',
          portfolio: [
            {
              id: '1',
              name: 'projection',
              src: 'http://v5.juanrod.co',
              img:'../../src/assets/images/projection.png'
            },
            {
              id: '2',
              name: 'out-of-the-box',
              src: 'http://v4.juanrod.co',
              img:'../../src/assets/images/out_of_box.png'
            },
            {
              id: '3',
              name: 'brutal-lite',
              src: 'http://v3.juanrod.co',
              img:'../../src/assets/images/brutal_lite.png'
            },
            {
              id: '4',
              name: 'b&w',
              src: 'http://v2.juanrod.co',
              img:'../../src/assets/images/b&w.png'
            },
            {
              id: '5',
              name: 'first juan',
              src: 'http://v1.juanrod.co',
              img:'../../src/assets/images/first_juan.png'
            }
          ]
        },
        {
          name: 'work',
          portfolio : [
            {
              id: '6',
              name: 'MediaScienceNYC',
              link: 'www.mediasciencenyc.com'
            }

          ]
        }
      ],
      activeImage : 0,
      showImage : false
    }
  },
  computed:{
    currentImage() {
          return this.projects[0].portfolio[this.activeImage].img;
      }
  },
  methods:{
    activateImage(imageIndex) {
      console.log('imageIndex:',imageIndex)
          this.showImage = !this.showImage
          this.activeImage = imageIndex;
      }
    // enter (e) {
    //   let projectImg = document.querySelector('.portfolio__img')
    //   console.log('projectImg:',projectImg)
    //   this.showImage = true
    //   console.log('enter:',e.target.parentElement.nextElementSibling.classList[1])
    //   let x = document.getElementById("myImg").alt;
    // },
    // leave (e) {
    //   console.log('leave:',e)
    // }
  }
}
</script>

<style>

</style>
