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
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: minmax(auto, 100px);
  grid-gap: 10px;

  grid-template-areas:
    'header header header'
    '   a    main    b   '
    '   .     .      .   '
    'footer footer footer';
}

::v-deep .item {
  &--1 {
    grid-area: header;
  }

  &--2 {
    grid-area: a;
  }

  &--3 {
    grid-area: main;
  }

  &--4 {
    grid-area: b;
  }

  &--5 {
    grid-area: footer;
  }
}

/* gird-{column, row}를 통해서 레이아웃 자유롭게 표현하기
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
} */
</style>
