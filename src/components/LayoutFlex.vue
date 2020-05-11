<template>
  <Container display-type="flex" />
</template>

<script>
import Container from './Container'

export default {
  name: 'LayoutFlex',
  components: {
    Container
  }
}
</script>

<style lang="scss" scoped>
::v-deep .container--flex {
  display: flex;
  flex-flow: row wrap; // Short-hand: flex-direction | flex-wrap
  justify-content: flex-start;
}

::v-deep .item {
  margin: 5px;
  flex: 1 1 calc(33.33% - 10px);
  height: 150px;
}
</style>
