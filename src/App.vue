<template>
  <div class="app-container">
    <div v-if="currentPage === 'home'" class="menu-container">
      <div class="header">
        <div class="left-nav">
          <span class="nav-item" @click="goTo('about')">About</span>
        </div>
        <span class="nav-item right" @click="goTo('developers')">Devs</span>
      </div>

      <div class="main-content">
        <button class="arrow" @click="prev">&#8592;</button>
        <div class="game-box">
          <div class="button-a">A</div>
          <div class="game-label">Game</div>
        </div>
        <button class="arrow" @click="next">&#8594;</button>
      </div>

      <div class="genre">
        <div>Game Genre: Action</div>
        <div class="genre-name">Developer: Lorem Ipsum</div>
      </div>
    </div>

    <div v-else-if="currentPage === 'about'" class="content-card">
      <h1>About Page</h1>
      <button class="back-button" @click="goTo('home')">Back</button>
    </div>

    <div v-else-if="currentPage === 'developers'" class="content-card">
      <div class="small-rectangles">
        <div class="small-rectangle">
          <img src="/Users/zacharybates/Desktop/Vue/Project1_Initial_Proto/public/Travis.jpg" class="dev-img">
          <p class="dev-desc">Travis: A passionate and creative game developer</p>
          <img src="/Users/zacharybates/Desktop/Vue/Project1_Initial_Proto/public/QR1.png" class="dev-img">
        </div>
        <div class="small-rectangle">
          <img src="/Users/zacharybates/Desktop/Vue/Project1_Initial_Proto/public/BuffTravis.jpg" class="dev-img">
          <p class="dev-desc">Buff Travis: Travis but so buff it looks fake</p>
          <img src="/Users/zacharybates/Desktop/Vue/Project1_Initial_Proto/public/QR2.png" class="dev-img">
        </div>
        <div class="small-rectangle">
          <img src="/Users/zacharybates/Desktop/Vue/Project1_Initial_Proto/public/image-2.png" class="dev-img">
          <p class="dev-desc">Saaf Sivart: The evil version of Travis</p>
          <img src="/Users/zacharybates/Desktop/Vue/Project1_Initial_Proto/public/QR3.png" class="dev-img">
        </div>
      </div>
      <button class="back-button" @click="goTo('home')">Back</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      currentPage: 'home'
    }
  },
  methods: {
    goTo(page) {
      this.currentPage = page;
    },
    prev() {
      // prev game
    },
    next() {
      //  next game
    }
  }
}
</script>

<style>
body, html, #app {
  margin: 0;
  padding: 0;
  height: 100%;
}

.app-container {
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(to bottom, #1E1E1E, #251C53);
  color: white;
  text-align: center;
  font-family: sans-serif;
}

.content-card {
  background-color: #40519D;
  padding: 2rem;
  border-radius: 1rem;
  height: 550px;
  width: 800px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.small-rectangles {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  width: 100%;
  align-items: center;
  margin-top: 1rem;
}

.small-rectangle {
  width: 600px;
  min-height: 150px;
  background-color: #1E1E1E;
  border-radius: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: space-around;
  padding: 1rem;
  gap: 1rem;
}

.dev-img {
  width: 100px;
  height: 100px;
  object-fit: cover;
  border-radius: 0.5rem;
}

.dev-desc {
  flex: 1;
  text-align: center;
}

.back-button {
  margin-top: 20px;
  padding: 10px 20px;
  background-color: #88aaff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  color: #1E1E1E;
}

.menu-container {
  padding: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  color: #7572a1;
  font-size: 1.2em;
}

.left-nav {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.nav-item {
  cursor: pointer;
}

.main-content {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 40px 0;
}

.arrow {
  background: none;
  border: none;
  color: #c51878;
  font-size: 2em;
  cursor: pointer;
}

.game-box {
  background: #dcdcdc;
  color: black;
  padding: 20px;
  margin: 0 20px;
  position: relative;
  width: 200px;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.button-a {
  background: #3a2c91;
  border-radius: 50%;
  color: white;
  width: 30px;
  height: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 10px;
}

.genre {
  font-size: 1.5em;
}

.genre-name {
  font-size: 2em;
  font-weight: bold;
  margin-top: 10px;
}
</style>
