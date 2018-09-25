<template lang="pug">
  section.footer-container
    div.inner-content
      div.image
        img(src="../../assets/img/vertical-branco.png")
      div.coming-soon
        q-icon(name="mdi-timer", color="teal-4", size="70px")
        p More informations soon...
      div.form
        h4.contact Contact
        form(action="https://formspree.io/contato@legalabs.com.br", method="POST", target="_blank").fields
          q-input(color="grey-8", placeholder="Nome", :value="name", name="Nome", required, inverted)
          q-input(color="grey-8", placeholder="Email", name="Email", :value="email", required, inverted)
          q-input(color="grey-8", placeholder="Mensagem", type="textarea", name="Mensagem", :value="message", :max-height="200", required, inverted)
          q-btn(color="primary").send-btn Send
    div.copyrigth
      div.inner-copy
        p AI CAMP 2018 © TODOS OS DIREITOS RESERVADOS
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
.image
  width 160px
  img
    max-width 150px
.coming-soon
  width 33%
  display flex
  flex-direction column
  justify-content center
  align-items center
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
  @media (max-width: 414px)
    padding-left 0
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
.inner-copy
  max-width 1233px
  p
    margin 0
    color $grey-7
    font-size 11px
.send-btn
  margin 0 0 0 auto
  display block
</style>
