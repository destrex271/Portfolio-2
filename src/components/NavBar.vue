<template>
  <div class="navbox">
    <div class="left">
      <img src="@/assets/logo.jpg" class="logo" @click="toSection('landing')" />
    </div>
    <div class="right">
      <a class="nav-item" @click="toSection('about-dev')">About Me </a>
      <a class="nav-item" @click="toSection('blogs')"> Blogs </a>
      <a class="nav-item" @click="toSection('projects')"> Projects</a>
      <a class="nav-item" @click="toSection('music')"> Music </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  methods: {
    toSection: (val) => {
      document.getElementById(val).scrollIntoView({ behavior: 'smooth' })
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap');

.navbox {
  display: flex;
  height: 10vh;
  width: 100%;
  position: sticky;
  background: #000;
  top: 0;
}

.left {
  display: flex;
  width: 50%;
  height: inherit;
  justify-content: flex-start;
  align-content: center;
}

.right {
  display: flex;
  width: 50%;
  height: inherit;
  justify-content: flex-end;
  align-content: center;
  flex-wrap: wrap;
}

.logo {
  /* margin: 1rem; */
  margin-left: 2rem;
  margin-top: 2rem;
}

.logo:hover {
  cursor: pointer;
}

.nav-item {
  color: white;
  font-family: 'Share Tech Mono', monospace;
  padding-left: 1.5rem;
  padding-right: 1.5rem;
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
  border-radius: 10px;
  text-decoration: none;
}

.nav-item:hover {
  color: black;
  cursor: pointer;
  background: white;
}

@media screen and (max-width: 900px) {
  .navbox {
    flex-direction: column;
    height: 15vw;
  }

  .left {
    display: none;
  }

  .right {
    width: 100%;
    /* margin-top: 3rem; */
    justify-content: center;
    align-items: flex-start;
  }

  .nav-item {
    padding-left: 1rem;
    padding-right: 1rem;
  }
}
</style>
