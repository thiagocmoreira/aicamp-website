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
        div.animation
          img(src="../../assets/img/ai3.png").circuit
          img(src="../../assets/img/ai2.png").move
          img(src="../../assets/img/ai1.png").machine
        div.content-list
          h2.title Content
          div.separator.other
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
    &.other
      background #1dffd4
      width 100%
      height 5px
  p
    color $tertiary
  .img
    max-width 380px
    margin-left 25px
  .content
    margin 20px auto 0 auto
    width 100%
    display flex
    .animation
      position relative
      width 300px
      height 330px
      margin-top -30px
      margin-right 50px
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
</style>
