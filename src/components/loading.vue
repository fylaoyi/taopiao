<template>
  <div class="loading" :style="{'width':this.width + 'px', 'height':this.height + 'px'}">
    <span class="circle">
    </span>
    <span class="circle-text">{{ msg }}</span>
  </div>
</template>

<script>
export default {
  name: 'loading',
  data () {
    return {
      width: 100,
      height: 100
    }
  },
  props: {
    msg: {
      default: 'loading...'
    }
  }
}
</script>

<style lang="less" scoped>
  @lineHeight: 100px;
  .loading{
    position: fixed;
    top:50%;
    left:50%;
    transform: translate(-50%, -50%);
    border-radius:4px;
    line-height: @lineHeight;
    background: rgba(0,0,0,.3);
    text-align: center;
    .circle{
      display: inline-block;
      border-top-color: rgb(255, 255, 255);
      border-left-color: rgb(255, 255, 255);
      border-bottom-color: rgb(255, 255, 255);
      border-width:4px;
      border-style:solid;
      width:30px;
      height:30px;
      z-index:200;
      margin:0 auto;
      border-radius:50%;
      vertical-align: middle;
      animation: loading 2s linear  infinite;
    }
    @keyframes loading{
      0% {
        transform: rotate(0deg);
      }
      100% {
        transform: rotate(360deg);
      }
    }
    .circle-text{
      color:#ffffff;
    }
  }
</style>
