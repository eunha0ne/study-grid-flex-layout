<template>
  <section>
    <h2>DISPLAY: GRID</h2>
    <div class="container container--grid">
      <div v-for="i in 5" :key="i" :class="`item item--${i}`">
        <span class="item__tag">ITEM--{{ i }}</span>
      </div>
    </div>
  </section>
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
  &--grid {
    display: grid;
    /* grid-template-columns: 250px 250px 250px 250px 250px 250px; */
    /* Short-hand: */
    /* grid-template-columns: repeat(5, 250px); */
    grid-template-columns: 1fr 2fr 3fr;
    grid-template-rows: 100px 200px;
    grid-gap: 30px;
  }
}
</style>
