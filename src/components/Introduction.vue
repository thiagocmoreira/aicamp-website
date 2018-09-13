<template lang="pug">
  q-page(:class="[(lightMode ? 'light-mode' : '')]").introduction-container
    vue-particles(
      :key="lightMode ? '1' : '2'"
      :color="lightMode ? '#333' : '#fff'",
      :particlesNumber="lightMode ? 200 : 160",
      :lineLinked="false",
      :moveSpeed="1",
      hoverMode="none",
      clickMode="repulse"
    )
    q-btn(
      :icon="lightMode ? 'mdi-lightbulb-on' : 'mdi-lightbulb'",
      :color="lightMode ? 'grey-5' : 'grey-9'",
      round,
      size="12px",
      @click="changeLight"
    ).btn-light.animate-pop
    div.content
      img(:src="lightMode ? '../assets/img/AI-Camp-preto.png' : '../assets/img/AI-Camp-branca.png'").logo.animate-pop
      countdown(:time="congress - now").animate-pop
        template(slot-scope="props")
          div.timer
            span.time-slot
              div.date {{ props.days }}
              div.date-description days
            span.time-slot
              div.date {{ props.hours }}
              div.date-description hours
            span.time-slot
              div.date {{ props.minutes }}
              div.date-description minutes
            span.time-slot
              div.date {{ props.seconds }}
              div.date-description seconds
</template>

<script>
import Vue from 'vue'
import VueParticles from 'vue-particles'
import VueCountdown from '@xkeshi/vue-countdown'
Vue.use(VueParticles)
Vue.component(VueCountdown.name, VueCountdown)

export default {
  name: 'Introduction',
  data () {
    return {
      now: new Date().getTime(),
      congress: new Date('2018-09-26 18:40:00 GMT-0300').getTime(),
      lightMode: true
    }
  },
  methods: {
    changeLight () {
      this.lightMode = !this.lightMode
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
  background linear-gradient(to right, #252525,#353535)
  width 100%
  &.light-mode
    background linear-gradient(to right, #cecece, white)
    span
      color #252525
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
span
  font-size 30px
  color white
  margin-top 30px
  display inline-block
  font-family BebasNeue
  font-weight bold
  letter-spacing 1.5px
.timer
  display flex
.time-slot
  margin 0 10px
  display flex
  flex-direction column
  align-items center
.date
  font-size 36px
.date-description
  font-size 10px
.btn-light
  position absolute
  top 0
  right 0
  margin 15px
</style>
