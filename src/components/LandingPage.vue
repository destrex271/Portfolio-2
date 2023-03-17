
<template>
  <div class="main-box">
    <div class="headbox">
      <div class="pr">Hi There! <span class="highlight">I Am</span></div>
      <div class="head">Akshat Jaimini</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LandingPage',
  components: {
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap');

.main-box {
  background-color: black;
  display: flex;
  width: 100%;
  height: 100vh;
  justify-content: center;
  align-items: center;
}

.headbox {
  width: fit-content;
  height: fit-content;
  color: white;
  justify-content: center;
  display: flex;
  flex-direction: column;
  position: relative;
}

.pr {
  font-family: 'Share Tech Mono', monospace;
  letter-spacing: 2px;
  font-size: 1.5rem;
  display: flex;
}

.highlight {
  background: white;
  color: black;
  padding-left: 3px;
  padding-right: 1px;
}

.head {
  font-family: "library3am";
  font-weight: bold;
  font-size: 5rem;
  letter-spacing: 5px;
}

.head::after {
  content: '';
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #fff;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

.head:hover::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

@media (max-width: 900px) {
  .headbox {
    justify-content: center;
  }

  .head {
    text-align: center;
  }

  .pr {
    justify-content: center;
    align-items: center;
    text-align: center;
    padding-bottom: 2rem;
  }
}
</style>
