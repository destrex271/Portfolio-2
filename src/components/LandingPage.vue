<template>
  <div class="main-body">
    <div class="left-box">
      <LandingText />
    </div>
    <div class="right-box"></div>
  </div>
</template>

<script>
import LandingText from './LandingText.vue';

export default {
  name: 'LandingPage',
  components: {
    LandingText,
  },
  methods: {
  },
}
</script>

<style>
.main-body {
  display: flex;
  flex-direction: row;
  height: 100vh;
  background-color: #f8f8f8;
}

.left-box {
  display: flex;
  width: 50vw !important;
  animation: 1s ease-out 0s 1 slideFromTop;
  height: 100vh;
  background-color: transparent;
  justify-content: center;
  align-items: center;
}

.right-box {
  display: flex;
  width: 50vw;
  animation: 1s ease-out 0s 1 slideFromTop;
  height: 100vh;
}

@keyframes slideFromTop {
  0% {
    transform: translateY(-100%);
  }

  100% {
    transform: translateY(0);
  }
}
</style>
