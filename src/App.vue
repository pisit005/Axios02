<template>
  <div id="app">
    <img src="https://img.icons8.com/ios/100/000000/infinity-large.png" height="150px"/>
    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <anime/>
  </div>
</template>

<script>

import anime from './components/anime.vue'

export default {
  name: 'App',
  components: {

    anime
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
