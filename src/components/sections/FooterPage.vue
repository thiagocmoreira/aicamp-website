<template lang="pug">
  section.footer-container
    div.inner-content
      div.image
        img(src="../../assets/img/vertical-branco.png")
      div.coming-soon
        q-icon(name="mdi-timer", color="teal-13", size="70px")
        p {{$t('footer.informationsSoon')}}
      div.form
        h4.contact {{$t('footer.contact')}}
        form(action="https://formspree.io/contato@legalabs.com.br", method="POST", target="_blank").fields
          q-input(color="grey-8", :placeholder="$t('footer.field1')", :value="name", name="Name", required, inverted)
          q-input(color="grey-8", :placeholder="$t('footer.field2')", name="Email", :value="email", required, inverted)
          q-input(color="grey-8", :placeholder="$t('footer.field3')", type="textarea", name="Message", :value="message", :max-height="100", required, inverted)
          q-btn(color="primary", type="submit").send-btn {{$t('footer.send')}}
    div.copyrigth
      div.inner-copy
        p {{$t('copyright')}}
</template>

<script>
export default {
  name: 'FooterPage',
  data () {
    return {
      name: '',
      company: '',
      email: '',
      message: ''
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~variables'
.footer-container
  display flex
  flex-direction column
  background $tertiary
  width 100%
  font-family OpenSans
.inner-content
  padding 40px 0
  width 90%
  max-width 1233px
  margin 0 auto
  display flex
  flex-direction row
  @media (max-width: 860px)
    flex-wrap wrap
    justify-content center
  @media (max-width: 580px)
    flex-direction column
    align-items center
.image
  width 160px
  img
    max-width 150px
    @media (max-width: 782px)
      margin-bottom 60px
      margin-left 20px
    @media (max-width: 580px)
      margin 0
.coming-soon
  width 33%
  display flex
  flex-direction column
  justify-content center
  align-items center
  @media (max-width: 850px)
    margin 0 20px
  @media (max-width: 782px)
    margin-left 80px
  @media (max-width: 580px)
    margin 30px 0
  p
    color white
    font-size 20px
    font-family Adam
    text-align center
    width 220px
  .q-icon
    margin-bottom 20px
h4
  font-family Adam
  margin 0
  font-size 18px
  line-height 24px
  color white
  margin-bottom 10px
  text-align left
.form
  flex 1
  padding-left 10px
  display flex
  flex-direction column
  @media (max-width: 580px)
    padding-left 0
    width 100%
  .q-input
    margin-bottom 12px
    border-radius 5px
    font-size 14px
    padding 0 15px
    color $text
  .q-option-group
    color white
    font-size 14px
  .options
    display flex
    padding-bottom 10px
    justify-content space-between
    .label
      color #bbb
      padding-top 4px
      font-size 18px
.copyrigth
  background #1c1c1c
  padding 10px 20px
  margin 0
  @media (max-width: 580px)
    text-align center
.inner-copy
  max-width 1233px
  margin 0 auto
  p
    margin 0
    color $grey-7
    font-size 11px
    text-transform uppercase
.send-btn
  margin 0 0 0 auto
  display block
</style>
