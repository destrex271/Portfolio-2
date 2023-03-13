<script>
export default {
  name: 'NavBar'
}
</script>

<template>
  <div class="nav">
    <div class="seg-small-1">
      <button class="logo-btn">
        <img src="https://avatars.githubusercontent.com/u/59926121?v=4" class="avatar-logo" />
      </button>
    </div>
    <div class="seg-big">
      <div class="nav-item">Home</div>
      <div class="nav-item"> About Me</div>
      <div class="nav-item">Projects</div>
      <div class="nav-item">Blogs</div>
    </div>
    <div class="seg-small-2">
      <button class="nav-btn">
        Lets Meet!
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

.seg-small-1 {
  display: flex;
  width: 9%;
  align-items: center;
  justify-content: flex-start;
}

.seg-small-2 {
  display: flex;
  width: 9%;
  align-items: center;
  justify-content: flex-end;
}

.seg-big {
  display: flex;
  width: 50%;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
}


.nav-btn {
  width: 90%;
  /* background-color: #131263; */
  background-color: #4e1263;
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

.avatar-logo {
  width: 3.8rem;
  border-radius: 36px;
  cursor: pointer;
}

.logo-btn {
  border-radius: 36px;
  border: none;
  background-color: transparent;
}

.nav-item:hover {
  color: grey;
}

@media (max-width: 900px) {
  .seg-small {
    width: 20%;
  }

  .seg-big {
    width: 70%;
  }

  .avatar-logo {
    width: 2rem;
  }

  .nav-item {
    font-size: 1rem;
  }

  .nav-btn {
    width: 150%;
    font-size: 0.8rem;
  }
}
</style>
