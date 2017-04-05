<template>
  <div id="app">
    <img src="./images/logo.png">
    <hello></hello>
    <a href="detail.html">详情页</a>
  </div>
</template>

<script>
  import lib from '@/assets/js/lib.js'
  import Hello from '@/components/Hello/Hello'

  export default {
    name: 'app',
    components: {
      Hello
    }
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
