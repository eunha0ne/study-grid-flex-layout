<template>
  <div class="container container--gird">
    <div v-for="i in 5" :key="i">item-{{ i }}</div>
  </div>
</template>

<script>
export default {
  name: 'LayoutGrid'
}
</script>

<style scoped></style>
