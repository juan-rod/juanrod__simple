<template>
  <div class="block">
    <div class="name">
      <p>{{fname}}</p> 
      <p>{{lname}}</p>
    </div>
    <div class="projects">
      <div class="projects__list" v-for="project in projects" :key="project.id">
        <div>{{project.name}}
          <div v-for="portfolio in project.portfolio" :key="portfolio.id">
            {{portfolio.name}}
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
              link: 'http://v5.juanrod.co'
            },
            {
              name: 'out-of-the-box',
              link: 'http://v4.juanrod.co'
            },
            {
              name: 'brutal-lite',
              link: 'http://v3.juanrod.co'
            },
            {
              name: 'b&w',
              link: 'http://v2.juanrod.co'
            },
            {
              name: 'first juan',
              link: 'http://v1.juanrod.co'
            }
          ]
        },
        {
          name: 'MediaScienceNYC',
          link: 'www.mediasciencenyc.com'
        }
      ]
    }
  }
}
</script>

<style>

</style>
