<template>
  <section>
    <h2>DISPLAY: FLEX</h2>
    <div class="container container--flex">
      <div v-for="i in 5" :key="i" :class="`item item--${i}`">
        ITEM--{{ i }}
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
    // flex-direction: row;
    // flex-wrap: nowrap;
    // Short-hand:
    flex-flow: row nowrap;
  }
}

.item {
  margin: 0 (30px / 2);
  flex: 0 0 250px;
  // width: 250px;
  height: 150px;

  &:first-of-type {
    margin-left: 0;
  }

  &:last-of-type {
    margin-right: 0;
  }
}

.item--2 {
  flex-shrink: 0 !important;
}
</style>
