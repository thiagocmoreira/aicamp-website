<template lang="pug">
  q-page.index-container
    q-scroll-observable(@scroll="userHasScrolled")
    menu-index(v-show="menuVisibility", logoWidth="130px", :appear="true").menu-visible.animate-popup-down
    introduction
    introduction
</template>

<script>
import Introduction from '../components/Introduction'
import MenuIndex from '../components/menu/Menu'
export default {
  name: 'PageIndex',
  components: {
    Introduction,
    MenuIndex
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

<style lang="stylus" scoped>
@font-face
  font-family BebasNeue
  src url(../assets/fonts/BebasNeue/BebasNeue_Regular.ttf)
.index-container
  background #2b2b2b
.menu-visible
  position fixed
  top 0
  width 100%
  z-index 100
</style>
