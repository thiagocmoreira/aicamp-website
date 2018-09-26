<template lang="pug">
  q-slide-transition
    div.menu-mobile-container
      div.menu-list
        a(href="#", v-scroll-to="{ el: '#about-us', offset: -50}").scrollactive-item
          li {{$t('menu.aboutUs')}}
        a(href="#", v-scroll-to="{ el: '#content', offset: -110}").scrollactive-item
          li {{$t('menu.content')}}
        a(href="#", v-scroll-to="{ el: '#schedule', offset: -90}").scrollactive-item
          li {{$t('menu.schedule')}}
        a(href="#", v-scroll-to="'#professionals'")
          li {{$t('menu.professionals')}}
</template>

<script>
export default {
  name: 'MenuMobile'
}
</script>

<style lang="stylus" scoped>
.menu-mobile-container
  width 100%
  background #eee
  // box-shadow inset 0px -72px 16px -75px rgba(0,0,0,0.5)
  margin-top 0px
  .menu-list
    width 100%
    list-style-type none
    padding 0
    margin 0
    a
      text-decoration none
    li
      color #333
      padding 15px 20px
      border-bottom solid 1px #ccc
</style>
