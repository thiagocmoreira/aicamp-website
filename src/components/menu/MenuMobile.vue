<template lang="pug">
  q-slide-transition
    div.menu-mobile-container
      scrollactive(:offset="50").menu-list
        a(href="#about-us").scrollactive-item
          li {{$t('menu.aboutUs')}}
        a(href="#content").scrollactive-item
          li {{$t('menu.content')}}
        a(href="#schedule").scrollactive-item
          li {{$t('menu.schedule')}}
        a(href="#professionals")
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
