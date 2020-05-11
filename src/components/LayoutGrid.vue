<template>
  <div class="container container--gird">
    <div v-for="i in 5" :key="i" :class="`item item--${i}`">item--{{ i }}</div>
  </div>
</template>

<script>
export default {
  name: 'LayoutGrid'
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/item';
</style>
