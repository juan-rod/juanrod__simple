<template>
  <div class="scene slate">
    <div class="box show-front">
      <div class="box__face  box__face--front">
        <the-block v-show="showProject"></the-block>
        <!-- <img :src="blockImg" alt=""> -->
      </div>
      <div class="box__face box__face--back">back</div>
      <div class="box__face box__face--right"></div>
      <div class="box__face box__face--left">left</div>
      <div class="box__face box__face--top">top</div>
      <div class="box__face box__face--bottom">bottom</div>
    </div>
    <div id="box-right" class="box box--right show-front">
      <div class="box__face  box__face--front">
      </div>
      <div class="box__face box__face--back">back</div>
      <div class="box__face box__face--right"></div>
      <div class="box__face box__face--left">left</div>
      <div class="box__face box__face--top">top</div>
      <div class="box__face box__face--bottom">bottom</div>
    </div>
  </div>
</template>

<script>
import TheBlock from './Block.vue'
export default {
  name: 'slate',
  components: { TheBlock },
  data () {
    return {
      showProject: true,
      blockImg :'../../src/assets/images/projection.png'
    }
  }
}
</script>

<style>

</style>
