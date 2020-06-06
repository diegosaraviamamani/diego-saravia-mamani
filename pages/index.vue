<template>
  <div>
    <Home />
    <About />
    <Portfolio />
  </div>
</template>

<script>
import Home from '~/components/Home'
import About from '~/components/About'
import Portfolio from '~/components/Portfolio'

export default {
  components: { Home, About, Portfolio }
}
</script>
<style lang="scss" scoped>
</style>