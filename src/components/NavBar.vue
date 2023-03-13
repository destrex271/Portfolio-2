<script>
export default {
}
</script>

<template>
  <div class="nav">
    <div class="seg-small">
      <button class="logo-btn">
      </button>
    </div>
    <div class="seg-big">
      <div class="nav-item">Home</div>
      <div class="nav-item"> About Me</div>
      <div class="nav-item">Projects</div>
      <div class="nav-item">Blogs</div>
    </div>
    <div class="seg-small">
      <button class="nav-btn">
        Contact
      </button>
    </div>
  </div>
</template>


<style>
@import url('https://fonts.googleapis.com/css2?family=Rajdhani:wght@500&display=swap');

.nav {
  display: flex;
  position: absolute;
  top: 0;
  width: 100%;
  height: 10vh;
  background-color: transparent;
  z-index: 1;
  flex-direction: row;
  justify-content: center;
}

.seg-small {
  display: flex;
  width: 7%;
  align-items: center;
  justify-content: center;
}

.seg-big {
  display: flex;
  width: 50%;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
}

.nav-logo {}

.nav-btn {
  width: 100%;
  background-color: #1e1e1e;
  border: none;
  height: fit-content;
  font-family: 'Rajdhani', sans-serif;
  font-size: 1.2rem;
  color: white;
  padding: 0.5rem;
  border-radius: 10px;
  box-shadow: 0px 2px #000000a2;
}

.nav-btn:active {
  box-shadow: none;
  transform: translateY(4px);
}

.nav-item {
  font-family: 'Rajdhani', sans-serif;
  font-size: 1.2rem;
  cursor: pointer;
}

.logo-btn {
  border-radius: 36px;
  background-color: transparent;
  width: fit-content;
  height: fit-content;
}

.nav-item:hover {
  color: grey;
}
</style>
