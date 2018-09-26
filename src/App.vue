<template>
  <div id="q-app">
    <router-view />
  </div>
</template>

<script>
import Vue from 'vue'
import VueScrollactive from 'vue-scrollactive'
Vue.use(VueScrollactive)
export default {
  name: 'App'
}
</script>

<style>
</style>
