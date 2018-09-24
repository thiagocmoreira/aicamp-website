<template lang="pug">
  section.footer-container
    div.inner-content
      div.image
        img(src="../../assets/img/vertical-branco.png")
      div.social-media
        h4 Redes Sociais
        p Fique por dentro das novidades sobre o AI Camp em nossas redes sociais
        div.medias
          q-btn(icon="mdi-linkedin", round, color="white", flat, size="24px")
          q-btn(icon="mdi-instagram", round, color="white", flat, size="24px")
          q-btn(icon="mdi-facebook", round, color="white", flat, size="24px")
      div.form
        form(action="https://formspree.io/contato@legalabs.com.br", method="POST", target="_blank").fields
          q-input(color="white", placeholder="Nome", :value="name", name="Nome", required, inverted-light)
          q-input(color="white", placeholder="Empresa", name="Empresa", :value="company", required, inverted-light)
          q-input(color="white", placeholder="Email", name="Email", :value="email", required, inverted-light)
          q-input(color="white", placeholder="Mensagem", type="textarea", name="Mensagem", :value="message", :max-height="200", required, inverted-light)
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
  width 250px
  img
    max-width 150px
.social-media
  width 33%
  h4
    font-family Adam
    margin 0
    font-size 18px
    line-height 24px
    color white
    margin-bottom 10px
    text-align left
  p
    color white
    font-size 12px
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
