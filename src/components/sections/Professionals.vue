<template lang="pug">
  section.professionals-container#professionals
    div.inner-content
      h2.title  {{$t('professionals.title')}}
      div.professional
        q-card.border
          div.photo
            img(src="../../assets/img/Foto_Ricardo_Fernandes.jpg").ricardo
        div.description
          h3.title {{$t('professionals.ricardo.name')}}
          p {{$t('professionals.ricardo.description')}}
      div.professional.right
        div.description
          h3.title.right {{$t('professionals.fabricio.name')}}
          p {{$t('professionals.fabricio.description')}}
        q-card.border.right
          div.photo
            img(src="../../assets/img/FABRICIO.jpg")
      div.professional
        q-card.border
          div.photo
            img(src="../../assets/img/NILTON_CORREIA.jpg")
        div.description
          h3.title {{$t('professionals.nilton.name')}}
          p {{$t('professionals.nilton.description')}}
      div.professional.right
        div.description
          h3.title.right {{$t('professionals.kleber.name')}}
          p {{$t('professionals.kleber.description')}}
        q-card.border.right
          div.photo
            img(src="../../assets/img/Kleber.jpg")
      img(src="../../assets/img/Circulos.svg").circle-1
      img(src="../../assets/img/Circulos.svg").circle-2
</template>

<script>
export default {
  name: 'Professionals'
}
</script>

<style lang="stylus" scoped>
@import '~variables'
.professionals-container
  display flex
  flex-direction column
  padding 90px 0 60px 0
  background linear-gradient(to bottom, #ffffff, $grey-4)
  width 100%
  font-family OpenSans
  position relative
  overflow hidden
.inner-content
  width 90%
  max-width 1233px
  margin 0 auto
  display flex
  flex-direction column
.title
  font-family Adam
  margin 0
  font-size 42px
  line-height 48px
  color $tertiary
  text-align center
  margin-bottom 30px
  z-index 10
  @media (max-width: 680px)
    padding-bottom 10px
.professional
  display flex
  align-items center
  z-index 10
  @media (max-width: 910px)
    margin-bottom 30px
  @media (max-width: 680px)
    flex-direction column
    margin-bottom 40px
    &.right
      flex-direction column-reverse
.border
  overflow hidden
  border-radius 500px
  margin-right 20px
  width 210px
  height 210px
  border solid 4px #1dffd4
  display flex
  justify-content center
  align-items center
  @media (max-width: 680px)
    margin 0
    margin-bottom 20px
  &.right
    margin-left 20px
    margin-right 0
    @media (max-width: 680px)
      margin 0
      margin-bottom 20px
.photo
  overflow hidden
  border-radius 500px
  width 200px
  height 200px
  border solid 4px white
  img
    width 100%
    &.ricardo
      margin-top -60px
.description
  display flex
  flex-direction column
  flex 1
  .title
    font-family Adam
    margin 0
    font-size 24px
    line-height 32px
    color $tertiary
    margin-bottom 10px
    text-align left
    @media (max-width: 680px)
      text-align center
    &.right
      text-align right
      @media (max-width: 680px)
        text-align center
  p
    @media (max-width: 680px)
      text-align justify
.circle-1
  position absolute
  left 0
  top 0
  max-width 800px
  margin-left -250px
  opacity 0.5
.circle-2
  position absolute
  right 0
  bottom 0
  max-width 800px
  margin-right -250px
  opacity 0.8
  filter brightness(0) invert(1)
</style>
