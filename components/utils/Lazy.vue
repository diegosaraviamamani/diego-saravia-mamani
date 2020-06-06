<template>
  <v-lazy :options="{threshold: .5}" transition="fade-transition">
    <slot></slot>
  </v-lazy>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
</style>