<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <svg viewbox="0 0 300 300" width="300" height="300">
      <line :x1="x1" y1=100 x2=200 y2=200 stroke="black"></line>
    </svg>
    <div>
      <input type="range" v-model="x1">
    </div>
  </div>
  
</template>

<script>
export default {
  name: 'SVGWorld',
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
