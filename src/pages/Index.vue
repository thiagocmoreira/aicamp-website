<template lang="pug">
  q-page.index-container.flex.flex-center
    introduction
</template>

<script>
import Introduction from '../components/Introduction'
export default {
  name: 'PageIndex',
  components: {
    Introduction
  }
}
</script>

<style lang="stylus" scoped>
@font-face
  font-family BebasNeue
  src url(../assets/fonts/BebasNeue/BebasNeue_Regular.ttf)
.index-container
  background #2b2b2b
</style>
