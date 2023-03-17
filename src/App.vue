<script>
import LandingPage from './components/LandingPage.vue'
import NavBar from './components/NavBar.vue'

export default {
  name: 'App',
  components: {
    LandingPage,
    NavBar
  },
  methods: {
  }
}
</script>

<template>
  <div>
    <NavBar />
    <section id="Landing">
      <LandingPage />
    </section>
  </div>
</template>


<style>
body {
  margin: 0;
}

@font-face {
  font-family: "library3am";
  src: url('./fonts/Library 3 am.otf');
}
</style>
