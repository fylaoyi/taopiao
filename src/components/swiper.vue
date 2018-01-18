<template>
  <div id="banner-wrapper">
    <Swipe></Swipe>
    <SwipeItem></SwipeItem>
  </div>
</template>
<script>
import {Swipe, SwipeItem} from 'vue-swipe'
require('vue-swipe/dist/vue-swipe.css')
export default {
  name: 'banner',
  components: {
    Swipe,
    SwipeItem
  }
}
</script>

<style lang="less" scoped>
    #banner-wrapper{
        width:100%;
        height: 200px;
    }
</style>
