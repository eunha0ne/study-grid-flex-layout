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
  // grid-template-columns: repeat(5, 250px); // Short-hand: 250px 250px 250px 250px 250px 250px;
  grid-template-columns: 1fr 2fr 3fr;
  grid-template-rows: 100px 200px;
  grid-gap: 30px;
}
</style>
