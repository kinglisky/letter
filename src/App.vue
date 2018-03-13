<template>
  <div id="app">
    <div class="wrapper" ref="wrapper">
      <div class="depth-item level0" data-depth="0.6">
        <img src="./assets/yun.png">
      </div>
      <div class="depth-item level1" data-depth="0.8">
        <img src="./assets/yu0.png">
      </div>
    </div>
  </div>
</template>

<script>
import Rellax from 'rellax'
import Parallax from 'parallax-js'
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },

  mounted () {
    console.log(Rellax)
    // const rellaxList = new Rellax('.rellax', { center: false })
    const parallaxInstance = new Parallax(this.$refs.wrapper)
  }
}
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
}
html,
body {
  overflow: hidden;
  height: 100%;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  padding: 0;
  list-style-type: none;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

#app {
  overflow: hidden;
  height: 100%;
  color: #2c3e50;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  background-color: #85dee8;

  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.wrapper {
  height: 100%;
}

.depth-item {
  position: relative;
  width: 100%;
  height: 100%;

  img {
    position: absolute;
  }
}
.level0 {
  // border: 1px solid #ccc;
  img {
    width: 120%;
    left: -10%;
    bottom: -10%;
  }
}
.level1 {
  img {
    top: 30%;
    right: -2%;
    width: 100%;
    max-width: 1000px;
  }
}
</style>
