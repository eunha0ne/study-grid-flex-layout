<template>
  <Container display-type="grid" />
</template>

<script>
import Container from './Container'

export default {
  name: 'LayoutGrid',
  components: {
    Container
  }
}
</script>

<style lang="scss" scoped>
::v-deep .container--grid {
  display: grid;
  /* Short-hand: 20% 20% 20% 20% 20%; */
  grid-template-columns: repeat(5, 1fr);
  /* grid-template-rows: 100px 100px; */
  grid-auto-rows: minmax(auto, 100px);
  grid-gap: 10px;
}

::v-deep .item {
  &--1 {
    grid-column: 1 / 4;
  }

  &--2 {
    grid-column: 1 / 1;
    grid-row: 2 / 4;
  }

  &--4 {
    grid-column: 4 / 6;
    grid-row: 3 / 5;
  }

  &--5 {
    grid-column: 3 / 6;
  }
}
</style>
