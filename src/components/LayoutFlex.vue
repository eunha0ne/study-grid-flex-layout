<template>
  <div class="container container--flex">
    <div v-for="i in 5" :key="i" :class="`item item--${i}`">item--{{ i }}</div>
  </div>
</template>

<script>
export default {
  name: 'LayoutGrid'
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/container';
@import '@/assets/styles/item';

.container {
  &--flex {
    display: flex;
    flex-direction: row;
  }
}

.item {
  width: 250px;
  height: 150px;
}
</style>
