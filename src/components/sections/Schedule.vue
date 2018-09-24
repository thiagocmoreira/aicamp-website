<template lang="pug">
  section.schedule-container#schedule
    h2.title Schedule
    div.black
      div.inner-content
        img(src="../../assets/img/Schedule.svg")
    div.cards
      q-card.card
        h3.card-title Cutting Edge
        img(src="../../assets/img/Diamante.svg")
        p Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.
      q-card.card
        h3.card-title MVP Challenger
        img(src="../../assets/img/quebra-cabecas.svg")
        p The MVP Challenge is the last phase of the training program organized in the form of a competition. Its start coincides with the disclosure of problems that have to be solved. At the end of 4 weeks the models developed by the competitors by the are assessed against the part of the dataset designated for the validation.
      q-card.card
        h3.card-title Awards
        img(src="../../assets/img/Medalha.svg")
        p As an award, the engineer owner of the best model will receive the prize of R $ 1500.00 per problem, and the engineer who achieves the best performance, considering All problems, will receive, in addition to the individual awards, the funding of the course of Advanced Machine Learning For Big Data and Text Processing offered by MIT, with all expenses paid.
</template>

<script>
export default {

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
.cards
  display flex
  margin 0 auto
  margin-top -300px
  width 90%
.card
  flex 1
  background linear-gradient(to bottom, $primary, #1dffd4)
  margin 0 20px
  padding 35px
  display flex
  flex-direction column
  align-items center
  max-width 360px
  img
    max-height 130px
  p
    text-align justify
.card-title
  font-family Adam
  margin 0
  font-size 36px
  line-height 40px
  color $tertiary
  text-align center
</style>
