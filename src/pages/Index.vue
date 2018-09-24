<template lang="pug">
  q-page.index-container
    q-scroll-observable(@scroll="userHasScrolled")
    menu-index(v-show="menuVisibility", logoWidth="130px", :appear="true").menu-visible.animate-popup-down
    introduction
    about-us
    schedule
    professionals
</template>

<script>
import MenuIndex from '../components/menu/Menu'
import Introduction from '../components/sections/Introduction'
import AboutUs from '../components/sections/AboutUs'
import Schedule from '../components/sections/Schedule'
import Professionals from '../components/sections/Professionals'
export default {
  name: 'PageIndex',
  components: {
    MenuIndex,
    Introduction,
    AboutUs,
    Schedule,
    Professionals
  },
  data () {
    return {
      menuVisibility: false,
      isMobile: false
    }
  },
  methods: {
    userHasScrolled (scroll) {
      if (!this.isMobile && scroll.position >= 45) {
        this.menuVisibility = true
      } else {
        this.menuVisibility = false
      }
    },
    onResize (size) {
      if (size.width < 901) {
        this.isMobile = true
      }
    }
  }
}
</script>

<style lang="stylus">
.index-container
  font-family OpenSans, Arial, Helvetica, sans-serif
</style>

<style lang="stylus" scoped>
@font-face
  font-family BebasNeue
  src url(../assets/fonts/BebasNeue/BebasNeue_Regular.ttf)
@font-face
  font-family Adam
  src url(../assets/fonts/ADAM_CG_PRO.otf)
@font-face
  font-family OpenSans
  src url(../assets/fonts/OpenSans/OpenSans-Regular.ttf)
.index-container
  background #2b2b2b
.menu-visible
  position fixed
  top 0
  width 100%
  z-index 100
</style>
