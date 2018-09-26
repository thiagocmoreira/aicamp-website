<template lang="pug">
  section.schedule-container#schedule
    h2.title {{$t('schedule.title')}}
    div.black
      div.inner-content
        img(src="../../assets/img/Schedule.svg")
    div.cards
      q-card.card
        h3.card-title {{$t('schedule.curringEdge.title')}}
        img(src="../../assets/img/Diamante.svg")
        p {{$t('schedule.curringEdge.text')}}
      q-card.card
        h3.card-title {{$t('schedule.mvpChallenger.title')}}
        img(src="../../assets/img/Quebra-cabecas.svg").qc
        p {{$t('schedule.mvpChallenger.text')}}
      q-card.card
        h3.card-title {{$t('schedule.awards.title')}}
        img(src="../../assets/img/Medalha.svg")
        p {{$t('schedule.awards.text')}}
</template>

<script>
export default {
  name: 'Schedule'
}
</script>

<style lang="stylus" scoped>
@import '~variables'
.schedule-container
  display flex
  flex-direction column
  padding 50px 0 0 0
  background white
  width 100%
  font-family OpenSans
.black
  width 100%
  background #231f20
  padding 50px 0 360px 0
.inner-content
  width 90%
  max-width 1233px
  margin 0 auto
  display flex
  flex-direction column
.title
  font-family Adam
  margin 0
  font-size 100px
  line-height 40px
  color $tertiary
  text-align center
  margin 0
  &.title-br
    font-size 70px
    line-height 40px
  @media (max-width: 650px)
    font-size 75px
    line-height 35px
  @media (max-width: 510px)
    font-size 55px
    line-height 23px
.cards
  display flex
  margin 0 auto
  margin-top -300px
  width 90%
  justify-content center
  @media (max-width: 1118px)
    flex-wrap wrap
    // max-width 800px
.card
  flex 1
  background linear-gradient(to bottom, $primary, #99ffec)
  margin 0 20px
  padding 35px
  display flex
  flex-direction column
  align-items center
  max-width 360px
  @media (max-width: 1200px)
    padding 25px
    margin 0 15px
    &:first-of-type
      margin-left 0
    &:last-of-type
      margin-right 0
  @media (max-width: 1118px)
    min-width 282px
    &:nth-of-type(2)
      margin-right 0
  @media (max-width: 1004px)
    &:last-of-type
      margin-top 30px
  @media (max-width: 740px)
    margin 0 0 30px 0 !important
    width 100%
    min-width 382px
    &:last-of-type
      margin-bottom 4px !important
  @media (max-width: 500px)
    min-width 280px
  img
    max-height 130px
    margin 15px 0
  p
    text-align justify
.card-title
  font-family Adam
  margin 0
  font-size 36px
  line-height 40px
  color $tertiary
  text-align center
.qc
  transform scale(0.8)
  margin 10px 0 !important
</style>
