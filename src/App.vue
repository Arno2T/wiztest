<template>
  <div id="app">
    <header-poc></header-poc>
    <timer></timer>
  </div>
</template>

<script>
import HeaderPoc from './components/Header.vue'
import Timer from './components/Timer.vue'
export default {
  name: 'app',
  components: {
    'header-poc': HeaderPoc,
    'timer': Timer
  }
}
</script>

<style lang="less">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}
</style>
