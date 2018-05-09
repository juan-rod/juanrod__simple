<template>
  <div class="block border">
    <div class="block__left border2">
      <div class="name border3">
        <p>{{fname}}</p> 
        <p>{{lname}}</p>
      </div>
      <div class="social border3">
        <h2>find me</h2>
        <div class="social__links" v-for="items in social" :key="items.id">
          <a class="" :href="items.src" target="_blank"><span class=""><i class="fa fa-lg" :class="items.icon"></i></span></a>
        </div>
      </div>
    </div>
    <div class="block__right border2">
      <div class="intro border3">
        <h1>hi. juan,here.</h1>
        <p>I am a front end developer in Austin, Texas. </p><p>I love creating something out of nothing. yeah, yeah, everyone says that and THEY SHOULD!</p>
      </div>
      <div class="projects border3">
        <h2>Stuff I'm working on</h2>
        <div class="projects__list border2" v-for="project in projects" :key="project.id">
          <div>{{project.name}}
            <div class="border3" v-for="portfolio in project.portfolio" :key="portfolio.id">
              <a class="" :href="portfolio.src" target="_blank"><p>{{portfolio.name}}</p></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name:'Block',
  data () {
    return {
      fname:'Juan',
      lname: 'Rodriguez',
      title: 'Front End Developer',
      projects:[
        {
          name: 'portfolio',
          portfolio: [
            {
              name: 'projection',
              src: 'http://v5.juanrod.co',
              img:''
            },
            {
              name: 'out-of-the-box',
              src: 'http://v4.juanrod.co',
              img:''
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
      social: [
        {
          name: 'LinkedIn',
          icon: 'fa-linkedin-square',
          src: 'https://www.linkedin.com/in/juanrod1'
        },
        {
          name: 'GitHub',
          icon: 'fa-github-square',
          src: 'https://github.com/juan-rod'
        },
        {
          name: 'Email',
          icon: 'fa-envelope-o',
          src: 'mailto:juan.j.rodriguez2@gmail.com?Subject=Hey%20Juan'
        }
      ]
    }
  }
}
</script>

<style>

</style>
