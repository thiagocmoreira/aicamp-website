<template lang="pug">
  q-page.introduction-container
    menu-index.menu-index
    div.content
      img(src="../assets/img/frente.png")
    vue-particles(
      color="#fff",
      :particlesNumber="160",
      :lineLinked="false",
      :moveSpeed="1",
      hoverMode="none",
      clickMode="repulse"
    )
</template>

<script>
import Vue from 'vue'
import VueParticles from 'vue-particles'
import VueCountdown from '@xkeshi/vue-countdown'
Vue.use(VueParticles)
Vue.component(VueCountdown.name, VueCountdown)

import MenuIndex from '../components/menu/Menu'

export default {
  name: 'Introduction',
  components: {
    MenuIndex
  },
  data () {
    return {
      now: new Date().getTime(),
      congress: new Date('2018-09-26 18:40:00 GMT-0300').getTime(),
      lightMode: true
    }
  },
  computed: {
    blackLogo () {
      return require('../assets/img/AI-Camp-preto.png')
    },
    whiteLogo () {
      return require('../assets/img/AI-Camp-branca.png')
    }
  }
}
</script>

<style lang="stylus">
.particles-js-canvas-el
  height 99vh !important
</style>

<style lang="stylus" scoped>
@import '~variables'
.introduction-container
  background-image url(https://images.unsplash.com/photo-1513112687946-67bc1c823f3a?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=05f28f8731c3274f7ed610e7f74b97c9&auto=format&fit=crop&w=1489&q=80)
  width 100%
.menu-index
  position absolute
  top 0
  width 100%
  z-index 99
  @media (max-width: 901px)
    position fixed
    top 0
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
</style>
