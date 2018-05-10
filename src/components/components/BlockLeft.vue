<template>
  <div class="block__left border2">
      <div class="name border3">
        <h3>{{fname}}</h3> 
        <h3>{{lname}}</h3>
      </div>
      <div class="social border3">
        <h2>find me</h2>
        <div class="social__links">
          <div class="social__links--icons" v-for="items in social" :key="items.id">
            <a class="" :href="items.src" target="_blank"><span class=""><i class="fa fa-lg" :class="items.icon"></i></span></a>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'BlockLeft',
  data () {
    return {
      fname:'Juan',
      lname: 'Rodriguez',
      title: 'Front End Developer',
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
