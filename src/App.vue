<template>
  <div id="app">
    <div class="header">
      <span class="area">北京</span>
      <span class="hot-on" @click="changeClass($event)">正在热映</span>
      <span class="hot-on" @click="changeClass($event)">即将上映</span>
    </div>
    <loading v-if="isShow"></loading>
    <movieList></movieList>
    <router-view/>
  </div>
</template>

<script>
// import banner from './components/swiper'
import loading from '@/components/loading'
import movieList from '@/components/movieList'

export default {
  name: 'App',
  data () {
    return {
      isShow: true
    }
  },
  components: {
    // banner,
    loading,
    movieList
  },
  methods: {
    changeClass: function (e) {
      e.target.className = 'active'
    }
  }

}
</script>

<style lang="less">
  *{
    padding:0;
    margin:0;
  }
  #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-size:12px;
  overflow: hidden;
    .header{
      width: 100%;
      height: 40px;
      line-height:40px;
      border-bottom:1px solid #f2f2f2;
      .area{
        display: inline-block;
        width:4rem;
      }
      .hot-on{
        display: inline-block;
        width: 6rem;
      }
    }
 }
 .active{
   border-bottom:2px solid #ff4d64;
 }
</style>
