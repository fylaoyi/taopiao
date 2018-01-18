<template>
  <div class="movieList">
      <ul>
          <li>
              <div class="left">
                  <img src="" alt="">
              </div>
              <div class="right">
                  <div class="title"></div>
                  <div class="director"></div>
              </div>
          </li>
      </ul>
  </div>
</template>
<script>
import axios from 'axios'
export default {
  name: 'movieList',
  data () {
    return {
      data: 123
    }
  },
  created () {
    this.init()
  },
  methods: {
    init: () => {
      axios.get('database/bj_hot.json').then((data) => {
        console.log(data)
      }, (err) => {
        console.log(err)
      })
      console.log(1)
    }
  }
}
</script>
