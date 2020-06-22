<template>
  <div id="app">
    <app-survey></app-survey>
  </div>
</template>

<script>
import AppSurvey from './components/AppSurvey.vue'

export default {
  name: 'App',
  components: {
    AppSurvey
  }
}
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
