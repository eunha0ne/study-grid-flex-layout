<template>
  <div id="app">
    <LayoutGrid />
  </div>
</template>

<script>
import LayoutGrid from './components/LayoutGrid.vue'

export default {
  name: 'App',
  components: {
    LayoutGrid
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
