<template>
  <div class="block__right border2">
    <div class="intro border3">
      <h1>hi. juan,here.</h1>
      <p>I am a front end developer in Austin, Texas. </p><p>I love creating something out of nothing. yeah, yeah, everyone says that and THEY SHOULD!</p>
    </div>
    <div class="projects border3">
      <h2>Stuff I'm working on</h2>
      <div class="projects__list border2" v-for="project in projects" :key="project.id">
        <div class="projects__main--title border3"><h3>{{project.name}}</h3></div>
        <div class="projects__sub border3">
          <div class="projects__sub--item border2" v-for="portfolio in project.portfolio" :key="portfolio.id" >
            <a class="" :href="portfolio.src" target="_blank" @mouseover="enter($event)" @mouseleave="leave($event)"><p>{{portfolio.name}}</p></a>
            <div :class="portfolio.name" class="portfolio__img" v-show="showImage">
              <img :src="portfolio.img" :alt="portfolio.name" :class="{ img__animation: showImage }">
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BlockRight',
  data () {
    return {
      projects:[
        {
          name: 'portfolio',
          portfolio: [
            {
              name: 'projection',
              src: 'http://v5.juanrod.co',
              img:'../../src/assets/images/projection.png'
            },
            {
              name: 'out-of-the-box',
              src: 'http://v4.juanrod.co',
              // img:'../../src/assets/images/out_of_box.png'
            },
            {
              name: 'brutal-lite',
              src: 'http://v3.juanrod.co',
              img:''
            },
            {
              name: 'b&w',
              src: 'http://v2.juanrod.co',
              img:''
            },
            {
              name: 'first juan',
              src: 'http://v1.juanrod.co',
              img:''
            }
          ]
        },
        {
          name: 'MediaScienceNYC',
          link: 'www.mediasciencenyc.com'
        }
      ],
      showImage: false
    }
  },
  computed:{
    portfolioClass (name) {
      console.log('name:',name)
      return 
    }
  },
  methods:{
    enter (e) {
      let projectImg = document.querySelector('.portfolio__img')
      console.log('projectImg:',projectImg)
      this.showImage = true
      console.log('enter:',e.target.parentElement.nextElementSibling.classList)
    },
    leave (e) {
      console.log('leave:',e)
    }
  }
}
</script>

<style>

</style>
