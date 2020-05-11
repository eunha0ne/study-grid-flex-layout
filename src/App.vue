<template>
  <div id="app">
    <LayoutGrid />
    <LayoutFlex class="l-m-top-60" />
  </div>
</template>

<script>
import LayoutGrid from './components/LayoutGrid.vue'
import LayoutFlex from './components/LayoutFlex.vue'

export default {
  name: 'App',
  components: {
    LayoutGrid,
    LayoutFlex
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

.l-m-top-60 {
  margin-top: 60px;
}
</style>
