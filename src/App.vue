<script>
import LandingPage from './components/LandingPage.vue'
import NavBar from './components/NavBar.vue'
import DeveLoper from './components/DeveLoper.vue'

export default {
  name: 'App',
  components: {
    LandingPage,
    NavBar,
    DeveLoper
  },
  data() {
    return {
      content: "Hello There! I am Akshat Jaimini, a sophomore Computer Science Student at Thapar Institute of Engineering and Technology. I am a computer enthusiast with special intrest in Open Source Technologies and Autmoation. I am also a Full Stack Developer(Web and Mobile) specializing in React.js, Vue.js, Node.js, Django and Actix Web. I am also experienced with App development in flutter and react native. Apart from this I am currently learning about Systems Programming and Computer Graphics."
    }
  },
  methods: {
  }
}
</script>

<template>
  <div>
    <NavBar />
    <section id="landing">
      <LandingPage />
    </section>
    <section id="about-dev">
      <DeveLoper :content="content" />
    </section>
  </div>
</template>


<style>
@import url('https://fonts.googleapis.com/css2?family=Major+Mono+Display&display=swap');

body {
  margin: 0;
  background: white;
}

body::-webkit-scrollbar {
  display: none;
}

@font-face {
  font-family: "library3am";
  src: url('./fonts/Library 3 am.otf');
}

@font-face {
  font-family: 'Banaras';
  src: url('./fonts/SAMAN___.TTF');
}

@font-face {
  font-family: 'Caviar';
  src: url('./fonts/CaviarDreams_Bold.ttf');
}
</style>
