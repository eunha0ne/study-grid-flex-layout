<template>
  <div id="app">
    <h1 class="app-title">Study grid and flex layout system.</h1>
    <LayoutGrid />
    <LayoutFlex class="l-mg-top-60" />
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
}

.app-title {
  margin: 60px 0;
  padding: 0 30px;
  font-size: 13px;
  text-align: left;
}

.l-mg-top-60 {
  margin-top: 60px;
}
</style>
