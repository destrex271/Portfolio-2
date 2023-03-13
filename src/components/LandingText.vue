<template>
  <div class="text-box">
    <h1 class="head linear-wipe">
      Hello There!
    </h1>
    <div class="buttons-bar">
      <button class="btn github">Explore Github!</button>
      <button class="btn resume">Download Resume</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "LandingText",
  methods: {}
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Rajdhani:wght@500&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@700&display=swap');

.text-box {
  width: 70%;
  height: 70%;
  font-family: 'Rajdhani', sans-serif;
  font-size: 1.4rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}

.buttons-bar {
  display: flex;
  flex-direction: row;
  width: 80%;
  justify-content: flex-start;
  align-items: center;
}

.btn {
  background-color: white;
  padding: 1rem 2rem;
  font-size: 1rem;
  letter-spacing: 1px;
  font-family: 'Rajdhani', sans-serif;
  border-radius: 10px;
  transition: background-color 0.3s ease-in-out;
}

.github {
  border: #d4e302 2px solid;
  margin-right: 2rem;
}

.github:hover {
  background-color: yellow;
}

.resume {
  border: #1e11ee 2px solid;
}


.resume:hover {
  background-color: #1e11ee;
  color: white;
}

.btn:active {
  transform: translateY(0.1rem);
}

.head {
  /* background: linear-gradient(-45deg, #6355a4, #6355a4, #e89a3e, #e89a3e); */
  background: linear-gradient(113.3deg, rgb(0, 98, 186) -6%, rgb(88, 40, 178) 10.2%, rgb(234, 39, 119) 34.3%, rgb(255, 80, 152) 54%, rgb(255, 101, 74) 62.5%, rgb(254, 166, 34) 77.2%, rgb(255, 227, 99) 91.2%, rgb(58, 243, 156) 112%, rgb(58, 243, 156) 118.1%);
  background-size: 300%;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 5vw;
  letter-spacing: 1px;
  text-transform: uppercase;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: animated_text 10s ease-in-out infinite;
  -moz-animation: animated_text 10s ease-in-out infinite;
  -webkit-animation: animated_text 10s ease-in-out infinite;
  padding-top: 0;
  padding-bottom: 0;
}

@media (max-width: 900px) {
  .text-box {
    margin-top: 10rem;
    width: 100%;
    justify-content: flex-start;
    align-items: center;
  }

  .head {
    font-size: 2.7rem;
  }
}

@keyframes animated_text {
  0% {
    background-position: 0px 50%;
  }

  50% {
    background-position: 100% 50%;
  }

  100% {
    background-position: 0px 50%;
  }
}
</style>
