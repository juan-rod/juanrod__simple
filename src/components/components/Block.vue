<template>
  <div id="block" class="block border">
    <block-left id="block__left"></block-left>
    <block-right id="block__right"></block-right>
  </div>
</template>

<script>
import BlockLeft from './BlockLeft.vue'
import BlockRight from './BlockRight.vue'
export default {
  name:'Block',
  components : { BlockLeft, BlockRight },
  data () {
    return {

      
    }
  }
}
</script>

<style>

</style>
