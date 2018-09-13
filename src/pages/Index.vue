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
.index-container
  background #2b2b2b
</style>
