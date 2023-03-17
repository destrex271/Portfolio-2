<script>
import LandingPage from './components/LandingPage.vue'

export default {
  name: 'App',
  components: {
    LandingPage
  },
  methods: {
  }
}
</script>

<template>
  <div>
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
