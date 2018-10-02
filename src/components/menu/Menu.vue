<template lang="pug">
  div.navbar-container
    q-card(:class="{appear: appear}").menu-container
      a(@click="$router.push('/')", title="Legal Labs").logo
        img(src="../../assets/img/logo-preta.png", :style="{ width: logoWidth }").logo-desk
        img(src="../../assets/img/logo-preta.png").logo-mobile
        img(src="../../assets/img/simbolo-azul.png").logo-mobile-small
      div.menu-items
        div(@click="changeLang").change-lang.btn-mobile.mobile-lang
          img(:src="brLang ? bandeiras2 : bandeiras1")
        q-btn(
          flat,
          dense,
          round,
          icon="menu"
          @click="showMenuMobile"
          aria-label="Menu",
          size="18px",
          color="grey-7"
        ).btn-mobile
        nav
          a(href="#", v-scroll-to="{ el: '#about-us', offset: -50}") {{$t('menu.aboutUs')}}
          a(href="#", v-scroll-to="{ el: '#content', offset: -110}") {{$t('menu.content')}}
          a(href="#", v-scroll-to="{ el: '#schedule', offset: -90}") {{$t('menu.schedule')}}
          a(href="#", v-scroll-to="'#professionals'") {{$t('menu.professionals')}}
          div(@click="changeLang").change-lang
            img(:src="brLang ? bandeiras2 : bandeiras1")
    menu-mobile(v-show="menuMobileVisibility && !isDesktop")
</template>

<script>
import MenuMobile from './MenuMobile'

export default {
  name: 'MenuIndex',
  components: {
    MenuMobile
  },
  data () {
    return {
      menuMobileVisibility: false,
      isDesktop: false
    }
  },
  props: {
    logoWidth: {
      type: String,
      default: '130px'
    },
    appear: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    changeLang () {
      if (this.$i18n.locale === 'ptBr') {
        this.$i18n.locale = 'en'
      } else {
        this.$i18n.locale = 'ptBr'
      }
    },
    showMenuMobile () {
      this.menuMobileVisibility = !this.menuMobileVisibility
    }
  },
  computed: {
    brLang () {
      return this.$i18n.locale === 'ptBr'
    },
    bandeiras1 () {
      return require('../../assets/img/bandeiras1.png')
    },
    bandeiras2 () {
      return require('../../assets/img/bandeiras2.png')
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~variables'
.navbar-container
  width 100%
.menu-container
  background white
  display flex
  flex-direction row
  justify-content space-between
  padding 25px 30px
  position relative
  border-radius 0
  &.appear
    padding 15px 20px
  @media (max-width: 900px)
    padding 12px 7px 9px 17px !important
    width 100%
    margin 0 auto
  @media (max-width: 360px)
    padding 15px 3px 9px 14px
  .logo
    transition all 0.2s ease
    &:hover
      cursor pointer
      transform scale(1.02)
    img
      width 100%
      height auto
      user-select none
      &.logo-desk
        display block
        @media (max-width: 999px)
          display none
      &.logo-mobile
        display none
        max-width 135px
        @media (max-width: 999px)
          display block
        @media (max-width: 401px)
          display none
      &.logo-mobile-small
        max-width 43px
        display none
        @media (max-width: 400px)
          display block
  .logo-partner
    position absolute
    top 0
    left 0
    display block
    margin-top 20px
    img
      max-width 80px
      height auto
      max-height 29px
  .menu-items
    display flex
    flex-direction row
    align-items center
    @media (max-width: 360px)
      margin-top -2px
    nav
      display inline-block
      margin-top -8px
      @media (max-width: 900px)
        display none
    .btn-mobile
      display none
      @media (max-width: 900px)
        display block
    a
      padding 0 15px
      list-style-type none
      text-transform uppercase
      font-weight 500
      color #444
      margin 0
      transition all 0.2s ease
      font-weight bold
      text-decoration none
      &:first-of-type
        padding-left 0
      &:last-of-type
        padding-right 0
      &:hover
        cursor pointer
        color $primary
.change-lang
  max-width 26px
  display inline-block
  margin-left 15px
  &.mobile-lang
    margin-right 5px
  img
    margin-bottom -7px
    width 100%
    cursor pointer
    transition all 0.2s ease
    &:hover
      transform scale(1.1)
.mobile-lang
  img
    margin-bottom -4px
.appear
  .menu-items
    nav
      margin-top 0
</style>
