<template lang="pug">
  q-page(ref="introduction").introduction-container
    q-scroll-observable(@scroll="userHasScrolled")
    q-parallax(:src="binary", :height="height")
    div.women
      div.color
      img(src="../../assets/img/women.png")
      div.color
    div.filter
    vue-particles(
      color="#cecece",
      :particlesNumber="160",
      :lineLinked="false",
      :moveSpeed="1",
      hoverMode="none",
      clickMode="repulse"
    ).particles
    div.content
      img(src="../../assets/img/frente.png").logo-big
      img(src="../../assets/img/vertical-branco.png").logo-vert
    p.we-are-there #wearethere
</template>

<script>
import Vue from 'vue'
import VueParticles from 'vue-particles'
Vue.use(VueParticles)

import MenuIndex from '../menu/Menu'

export default {
  name: 'Introduction',
  components: {
    MenuIndex
  },
  data () {
    return {
      menuVisibility: false,
      height: null
    }
  },
  computed: {
    blackLogo () {
      return require('../../assets/img/AI-Camp-preto.png')
    },
    whiteLogo () {
      return require('../../assets/img/AI-Camp-branca.png')
    },
    binary () {
      return require('../../assets/img/binary.png')
    }
  },
  mounted () {
    this.height = parseInt(this.$refs.introduction.layout.height)
  },
  methods: {
    userHasScrolled (scroll) {
      let { position } = scroll
      // let { direction, position } = scroll
      // if (direction === 'down') {
      //   this.height = parseInt(this.$refs.introduction.layout.height)
      // }
      if (position >= 40) {
        this.menuVisibility = true
      } else {
        this.menuVisibility = false
      }
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
  position relative
  display flex
  overflow hidden
.menu-index
  position absolute
  top 0
  width 100%
  z-index 99
  @media (max-width: 901px)
    position fixed
    top 0
.women
  position absolute
  top 0
  display flex
  height 100%
  width 100%
  img
    height 100%
    width auto
  .color
    flex 1
    height 100vh
    background #040404
.filter
  position absolute
  top 0
  background #262626
  width 100%
  height 100vh
  opacity 0.5
.particles
  position absolute
  top 0
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
.logo-big
  max-width 650px
  @media (max-width: 768px)
    max-width 500px
  @media (max-width: 414px)
    display none
.logo-vert
  display none
  max-width 170px
  @media (max-width: 414px)
    display block
.we-are-there
  font-family Adam
  position absolute
  bottom 0
  right 0
  color white
  font-size 32px
  margin 30px
  @media (max-width: 414px)
    font-size 20px
    margin 20px
</style>
