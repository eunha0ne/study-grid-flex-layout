<template>
  <section>
    <h2>DISPLAY: {{ displayType.toUpperCase() }}</h2>
    <div :class="[`container`, `container--${displayType}`]">
      <div v-for="i in 5" :key="i" :class="[`item`, `item--${i}`]">
        <span class="item__tag">ITEM--{{ i }}</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Container',
  props: {
    displayType: String
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/container';
@import '@/assets/styles/item';
</style>
