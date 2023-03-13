<template>
  <NavBar />
  <section>
    <LandingPage />
  </section>
</template>

<script>

import LandingPage from './components/LandingPage.vue'
import NavBar from './components/NavBar.vue';

export default {
  name: 'App',
  components: {
    LandingPage,
    NavBar
  }
}
</script>

<style>
body{
  margin: 0;
}
</style>
