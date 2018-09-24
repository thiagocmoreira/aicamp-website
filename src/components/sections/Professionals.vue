<template lang="pug">
  section.professionals-container#professionals
    div.inner-content
      h2.title Professionals Involved
      div.professional
        q-card.border
          div.photo
            img(src="../../assets/img/Foto_Ricardo_Fernandes.jpg").ricardo
        div.description
          h3.title RICARDO VIEIRA DE CARVALHO FERNANDES
          p Post-PH.D. in Legal Informatics at the CODEX: The Stanford Center for Legal Informatics, Stanford University. Founder of the Brazilian Institute of Artificial Intelligence. Professor Doctor of Law School at the University of Brasília (UnB). Executive Director of Legal.AI – Legal ArtiFicial Intelligence Research Group of UnB. Legal Labs’ Founder. Senior Researcher of ArtiFicial Intelligence at Legal Labs. AI Camp’s Founder.
      div.professional
        div.description
          h3.title.right FABRÍCIO BRAZ
          p Adjunct Professor of Software Engineering at Gama’s Faculty of the University of Brasília, he holds a PhD in Electrical Engineering, researching Project Standards for Software Security in partnership with the Security System Engineering Group of the University of Florida Atlantic. Since 2013 has been researching and in the field of machine learning focused on pattern detection.
        q-card.border.right
          div.photo
            img(src="../../assets/img/FABRICIO.jpg")
      div.professional
        q-card.border
          div.photo
            img(src="../../assets/img/NILTON_CORREIA.jpg")
        div.description
          h3.title NILTON SILVA
          p PhD in Data Processing and Environmental Analysis by the Institute of Geosciences of the University of Brasília. Two postdoctoral degrees in Computational Techniques for Temporal Analysis of Remote Sensing Images by the Universities of Brasilia and Washington. A postdoctoral stage in pattern recognition in time series of environmental data. He is a professor / researcher at the Faculty of Engineering of the University of Brasília (UnB), is a member of the editorial board of The International Journal of Forensic Computer Science and is a reviewer of the International Journal of Remote Sensing.
      div.professional
        div.description
          h3.title.right KLEBER
          p CIO of the Ministry of Transport, Ports and Civil Aviation; Ex-Director of ORACLE; Ex-Business Director of SERPRO; Ex-Business Administration Manager of ACCENTURE; Ex-Business Director of BearingPoint; Ex-Senior Specialist at the Finance Department of the IDB; Ex-General Coordinator of Information Technology for the Ministry of the Economy.
        q-card.border.right
          div.photo
            img(src="../../assets/img/Kleber.jpg")
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
  background white
  width 100%
  font-family OpenSans
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
.professional
  display flex
  align-items center
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
  &.right
    margin-left 20px
    margin-right 0
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
    &.right
      text-align right
</style>
