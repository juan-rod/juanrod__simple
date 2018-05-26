<template>
  <div class="block">
    <block-left></block-left>
    <block-right></block-right>
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
