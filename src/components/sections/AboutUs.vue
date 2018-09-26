<template lang="pug">
  section.about-us-container#about-us
    q-scroll-observable(@scroll="userHasScrolled")
    div.inner-content
      div.description-content
        div.description
          h2.title {{$t('aboutUs.title')}}
          div.separator
          p {{$t('aboutUs.text1')}}
          p {{$t('aboutUs.text2')}}
        div.image
          img(:class="[animateBrain ? ['show-brain', 'animate-pop'] : '']", src="../../assets/img/ai6.png").img
      div.content#content
        div.animation
          img(src="../../assets/img/ai3.png").circuit
          img(src="../../assets/img/ai2.png", :class="animateMode? 'move-down' : ''").move
          img(src="../../assets/img/ai1.png").machine
        div.content-list
          h2.title {{$t('content.title')}}
          div.separator.other
          ul.list
            li {{$t('content.list1')}}
            li {{$t('content.list2')}}
            li {{$t('content.list3')}}
            li {{$t('content.list4')}}
            li {{$t('content.list5')}}
            li {{$t('content.list6')}}
            li {{$t('content.list7')}}
</template>

<script>
export default {
  name: 'AboutUs',
  data () {
    return {
      animateBrain: false,
      animateMode: false,
      wasActivated: false
    }
  },
  mounted () {
    setInterval(() => { this.changeAnimate() }, 2000)
    this.isMobile = this.$q.platform.is.mobile
  },
  methods: {
    changeAnimate () {
      this.animateMode = !this.animateMode
    },
    userHasScrolled (scroll) {
      if (!this.isMobile && !this.wasActivated && scroll.position >= 230) {
        this.wasActivated = true
        this.animateBrain = true
      } else if (this.isMobile && !this.wasActivated && scroll.position >= 950) {
        this.wasActivated = true
        this.animateBrain = true
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~variables'
.about-us-container
  display flex
  flex-direction column
  padding 60px 0 40px 0
  background white
  width 100%
  font-family OpenSans
  .inner-content
    width 90%
    max-width 1233px
    margin 0 auto
    display flex
    flex-direction column
  .description-content
    display flex
    @media (max-width: 840px)
      flex-direction column
  .description
    position relative
  .title
    font-family Adam
    margin 0
    font-size 42px
    line-height 48px
    color $tertiary
  .separator
    // width calc(100% + 25px)
    background $primary
    height 4px
    margin 2px 0 25px 0
    width 100%
    &.other
      background #1dffd4
      height 5px
  p
    color $tertiary
  .img
    max-width 250px
    margin-left 25px
    visibility hidden
    @media (max-width: 840px)
      margin 20px auto 40px auto
      display block
  .content
    margin 20px auto 0 auto
    width 100%
    display flex
    @media (max-width: 840px)
      flex-direction column-reverse
    .animation
      position relative
      width 300px
      height 330px
      margin-top -30px
      margin-right 50px
      @media (max-width: 840px)
        margin 30px auto 20px auto
      .machine
        max-width 250px
        position absolute
        top 0
        right 0
      .move
        max-width 40px
        position absolute
        top 0
        right 0
        margin-right 204px
        margin-top 110px
        width 100%
        transition all 0.6s ease
      .circuit
        max-width 150px
        position absolute
        bottom 0
        left 0
  .content-list
    flex 1
  .list
    margin 0
    padding-left 20px
    li
      padding-left 10px
      list-style-type square
.move-down
  margin-top 170px !important
.show-brain
  visibility visible !important
</style>
