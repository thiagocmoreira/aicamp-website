<template lang="pug">
  q-page.introduction-container
    vue-particles(
      color="#fff",
      :particlesNumber="220",
      :lineLinked="false",
      :moveSpeed="1",
      hoverMode="none",
      clickMode="repulse"
    )
    div.content
      img(src="../assets/img/AI-Camp-branca.png").logo.animate-pop
</template>

<script>
import Vue from 'vue'
import VueParticles from 'vue-particles'
Vue.use(VueParticles)

export default {
  name: 'Introduction'
}
</script>

<style lang="stylus">
.particles-js-canvas-el
  height 99vh !important
</style>

<style lang="stylus" scoped>
@import '~variables'
.introduction-container
  background #2b2b2b
  width 100%
.content
  position absolute
  top 0
  width 100%
  height 100vh
  display flex
  flex-direction column
  align-items center
  justify-content center
  pointer-events none
.logo
  max-width 350px
  height auto
</style>
