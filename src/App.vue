<template>
  <section id="app">
    <ul class="parallax-wrapper" ref="wrapper">
      <li class="parallax-view" data-depth="0.1">
        <img class="cloud" src="./assets/cloud.png">
      </li>
      <li class="parallax-view" data-depth="0.2">
        <img class="whale" src="./assets/whale.png">
      </li>
      <li class="parallax-view" data-depth="0">
        <pre class="content">
日月星辰悄悄
湫兮如风
湫兮如风
升了又落
我却不知白天黑夜的存在
世界消失
有你在 我心里 真美好
有一天 想成为 你骄傲
日月星辰悄悄
升了又落我却不知白天黑夜的存在
世界消失
有你在 我心里 真美好
有一天 想成为 你的骄傲
今夕何夕 见此良人 如月之恒
为你守望 每次日落日升我一生都在用歌声寻觅你
为你享受着生命的悲喜请跟我乘风而去
我一生都在
用歌声寻觅你
为你享受着生命的悲喜
请跟我乘风而去
        </pre>
      </li>
      <div class="parallax-view" data-depth="0.6">
        <img class="paper-plane-1" src="./assets/paper_plane1.png">
      </div>
      <li class="parallax-view" data-depth="0.8">
        <img class="paper-plane-2" src="./assets/paper_plane2.png">
      </li>
    </ul>
    <ul class="extend-info">
      <li class="info-item github">GITHUB</li>
      <li class="info-item about-me">ABOUT ME</li>
    </ul>
  </section>
</template>

<script>
import Parallax from 'parallax-js'
export default {
  name: 'app',
  data () {
    return {
      msg: ''
    }
  },

  mounted () {
    const parallaxInstance = new Parallax(this.$refs.wrapper)
  }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
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
  background-color: #60dfed;

  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.parallax-wrapper,
.extend-info {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.parallax-view {
  position: relative;
  width: 100%;
  height: 100%;

  img {
    position: absolute;
  }

  .cloud {
    bottom: -5%;
    left: -10%;
    width: 120%;
  }

  .whale {
    top: 40%;
    right: -2%;
    width: 100%;
    max-width: 900px;
  }

  .content {
    position: absolute;
    top: 80px;
    left: 60px;
    width: 400px;
    height: 600px;
    padding: 16px;
    color: #445e68;
    line-height: 2;
    text-align: left;
    // border: 1px solid #000;
    // background: rgba(0, 0, 0, .5);
    // background: #ebeae7;
    border-radius: 4px;
  }

  .paper-plane-1 {
    top: 5%;
    left: 5%;
    width: 120px;
  }

  .paper-plane-2 {
    top: 80px;
    left: 100px;
    width: 120px;
  }
}

.extend-info {
  .info-item {
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 12px;
    border-radius: 50%;
    transition: box-shadow .3s ease-in-out;
    cursor: pointer;

    &:hover {
      box-shadow: 0 0 0 8px #ebeae7;
    }
  }

  .github {
    top: 100px;
    left: 800px;
    width: 80px;
    height: 80px;
    background: #ebeae7;
    background: #dd8071;
  }

  .about-me {
    top: 200px;
    left: 300px;
    width: 100px;
    height: 100px;
    background: #fef4de;
  }
}
</style>
