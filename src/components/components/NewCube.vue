<template>
  <div class="cube">
    <div class='cube__face'>
      <the-block></the-block>
    </div>
    <div class='cube__face'></div>
    <div class='cube__face'></div>
    <div class='cube__face'></div>
    <div class='cube__face'></div>
    <div class='cube__face'></div>
  </div>
</template>

<script>
import TheBlock from '../components/Block.vue'
export default {
  name: 'NewCube',
  components :{ TheBlock }
}
</script>

<style>

</style>
