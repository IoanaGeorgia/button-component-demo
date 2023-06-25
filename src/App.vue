<template>
  <div id="app">
    <LandingPage />
  </div>
</template>

<script>
import LandingPage from './components/LandingPage.vue'

export default {
  name: 'App',
  components: {
    LandingPage
  }
}
</script>

<style>

/* classes added to normalize the CSS */
#app * {
  padding:0px;
  margin:0px;
}
</style>
