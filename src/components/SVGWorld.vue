<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <svg viewbox="0 0 300 300" width="300" height="300">
      <line :x1="x1" y1=100 x2=200 y2=200 stroke="black"></line>
    </svg>
    <!-- https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/SVG_Image_Tag -->
    <svg width="600" height="300">
      <vue-flip width="300px" :active-click="true">
        <div slot="front">
          <image xlink:href="https://jp.vuejs.org/images/logo.png" width="300" height="300" />
        </div>
        <div slot="back">
          <image xlink:href="https://jp.vuejs.org/images/laravel.png" x="300" width="300" height="300" />
        </div>
      </vue-flip>
    </svg>
    <div>
      <input type="range" v-model="x1">
    </div>
    <vue-flip width="200px" :active-click="true">
      <div slot="front">
        <p>front</p>
      </div>
      <div slot="back">
        <p>back</p>
      </div>
    </vue-flip>
  </div>
  
</template>

<script>
import VueFlip from 'vue-flip'

export default {
  name: 'SVGWorld',
  components: {
    VueFlip
  },
  data () {
    return {
      msg: 'Welcome to SVG World',
      x1: 100
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
