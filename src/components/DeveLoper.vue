<template>
  <div class="main-box-dev">
    <div class="head-box-dev">
      <div class="dev-head">About Me</div>
    </div>
    <div class="dev-box">
      <div class="content-box">
        <ComputerScreen />
      </div>
      <div class="content-box">
        <div class="text-box">
          {{ this.content }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ComputerScreen from './ComputerScreen.vue'

export default {
  name: 'DeveLoper',
  props: ['content'],
  components: {
    ComputerScreen
  }
}
</script>

<style>
.main-box-dev {
  background-color: black;
  display: flex;
  flex-direction: column;
  height: 90vh;
}

.head-box-dev {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 10vh;
  color: #fefefe;
}

.dev-head {
  /* font-family: 'Banaras'; */
  font-family: 'Major Mono Display', monospace;
  font-size: 5rem;
  font-weight: semi-bold;
}

.dev-box {
  flex-direction: row;
  display: flex;
  height: 80vh;
}

.content-box {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50%;
  height: inherit;
  color: white;
  font-family: 'Share Tech Mono', monospace;
  font-size: 1.3rem;
}

.text-box {
  width: 85%;
  height: 80%;
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

@media screen and (max-width: 900px) {
  .main-box-dev {
    height: 150vh;
    padding-bottom: 10rem;
  }

  .head-box-dev {
    margin-top: 3rem;
    margin-bottom: 1.5rem;
  }

  .dev-head {
    font-size: 2.5rem;
  }

  .dev-box {
    flex-direction: column;
  }

  .content-box {
    width: 100%;
    height: 50%;
    padding-bottom: 10rem;
  }
}
</style>
