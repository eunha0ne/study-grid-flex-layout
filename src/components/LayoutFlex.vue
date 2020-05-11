<template>
  <section>
    <h2>DISPLAY: FLEX</h2>
    <div class="container container--flex">
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
  &--flex {
    display: flex;
    /* flex-direction: row; */
    /* flex-wrap: nowrap; */
    /* Short-hand: */
    flex-flow: row wrap;
    justify-content: flex-start;
  }
}

.item {
  margin: 15px;
  flex: 0 0 calc(33.33% - 30px);
  height: 150px;

  &:first-of-type {
    margin-left: 0;
  }

  &:last-of-type {
    margin-right: 0;
  }

  &:nth-of-type(3n + 1) {
    margin-left: 0;
  }
}
</style>
