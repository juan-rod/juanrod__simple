<template>
  <div class="scene">
    <div class="box show-front">
      <div class="box__face  box__face--front">
        <the-block></the-block>
      </div>
      <div class="box__face box__face--back">back</div>
      <div class="box__face box__face--right">right</div>
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
  components: { TheBlock }
}
</script>

<style>

</style>
