<template>
  <div class="box">
    <button class="button">Engineer</button>
    <button class="button">Producer</button>
  </div>
</template>

<script>
export default {
  name: "ButtonsBar"
}
</script>

<style>
/* @import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap'); */

.box {
  display: flex;
  flex-direction: row;
  width: fit-content;
  height: fit-content;
  justify-content: center;
  align-content: center;
  margin-top: 2rem;
  margin-bottom: -8rem;
}

.button {
  background-color: transparent;
  font-family: 'Share Tech Mono', monospace;
  border: 1px solid white;
  font-size: 1.2rem;
  color: white;
  width: 20rem;
  height: 4rem;
  margin: 3rem;
}

.button:hover {
  background: white;
  transition: background 0.3s ease-in;
  color: black;
  cursor: pointer;
}

.button:active {
  transform: translateY(0.1rem);
  transition: transform 0.3s ease-in-out;
}

@media screen and (max-width: 900px) {
  .box {
    flex-direction: column;
    margin-top: 3rem;
  }

  .button {
    margin: 0.5rem;
    width: 15rem;
  }
}
</style>
