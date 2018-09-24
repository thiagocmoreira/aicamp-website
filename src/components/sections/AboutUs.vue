<template lang="pug">
  section.about-us-container#about-us
    div.inner-content
      div.description-content
        div.description
          h2.title About Us
          div.separator
          p At this point, any relevant industry member or already owns its machine learning models in operation or are one step closer to it.
          p AI CAMP is a training program in natural language processing and deep learning, on real legal or governmental data, with duration of ve months and the objective of training high skilled AI engineers.
        div.image
          img(src="../../assets/img/about.jpg").img
      div.content#content
        h2.title Content
        ul.list
          li Structured literature review of the area.
          li Machine learning project strategy.
          li Collection, cleaning, labeling and expansion of the dataset.
          li Model training for an actual application.
          li Preparation for an eficient and organized process of experimentation.
          li Performing error analysis for model improvements.
          li Deployment of an AI product.
</template>

<script>
export default {
  name: 'AboutUs'
}
</script>

<style lang="stylus" scoped>
@import '~variables'
.about-us-container
  display flex
  flex-direction column
  padding 60px 0
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
  .description
    position relative
  .title
    font-family Adam
    margin 0
    font-size 42px
    line-height 48px
    color $tertiary
  .separator
    width calc(100% + 25px)
    background $primary
    height 4px
    margin 2px 0 25px 0
  p
    color $tertiary
  .img
    max-width 550px
    margin-left 25px
  .content
    background $grey-5
    margin 50px auto 0 auto
    padding 40px
    width 80%
    .title
      text-align center
      margin-bottom 10px
  .list
    margin 0
    li
      padding-left 10px
      list-style-type square
</style>
