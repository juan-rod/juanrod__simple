<template>
  <div class="block__right">
    <div class="intro border3">
      <h1>hi.</h1>
      <p>I am a front end developer. </p><p><i class="fa fa-map-marker" aria-hidden="true"></i> Austin, Texas. </p><p>I enjoy creating new stuff.</p>
    </div>
      <div class="projects border3">
        <h2>Speaking of</h2><h2> <i style="font-style: italic;">stuff</i></h2>
        <div class="projects__list" v-for="project in projects" :key="project.id">
          <div class="projects__main--title"><h3>{{project.name}}</h3></div>
          <div class="projects__sub border3">
            <div class="projects__sub--item" v-for="item in project.portfolio" :key="item.id" >
              <portfolio-list :item="item" ></portfolio-list>
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
              name: 'projection',
              src: 'http://v5.juanrod.co',
              img:'../../src/assets/images/projection.png'
            },
            {
              name: 'out-of-the-box',
              src: 'http://v4.juanrod.co',
              img:'../../src/assets/images/out_of_box.png'
            },
            {
              name: 'brutal-lite',
              src: 'http://v3.juanrod.co',
              img:'../../src/assets/images/brutal_lite.png'
            },
            {
              name: 'b&w',
              src: 'http://v2.juanrod.co',
              img:'../../src/assets/images/b&w.png'
            },
            {
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
              name: 'MediaScienceNYC',
              link: 'www.mediasciencenyc.com'
            }

          ]
        }
      ]
    }
  },
  computed:{
    portfolioClass (name) {
      console.log('name:',name)
      return 
    }
  },
  methods:{
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
