<template>
  <div class="app-container">
    <div class="content-card">
      <div v-if="currentPage === 'home'">
        <button class="nav-button" @click="currentPage = 'about'">About</button>
        <button class="nav-button" @click="currentPage = 'developers'">Developers</button>
      </div>
      
      <div v-if="currentPage === 'about'">
        <h2 class="page-title">About Page</h2>
        <button class="nav-button" @click="currentPage = 'home'">Back</button>
      </div>

      <div v-if="currentPage === 'developers'">
        <div class="small-rectangles">
          <div class="small-rectangle"></div>
          <div class="small-rectangle"></div>
          <div class="small-rectangle"></div>
        </div>
        <button class="nav-button" @click="currentPage = 'home'">Back</button>
      </div>
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
}

.content-card {
  background-color: #40519D;
  padding: 2rem;
  border-radius: 1rem;
  height: 550px;
  width: 800px;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
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
  width: 80%;
  height: 100px;
  background-color: #1E1E1E;
  border-radius: 0.5rem;
}

.nav-button {
  margin: 1rem;
  padding: 12px 24px;
  background-color: #8EBBFF;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 16px;
  cursor: pointer;
}

.nav-button:hover {
  background-color: #6b9de0;
}

.page-title {
  color: white;
  font-size: 24px;
  margin-bottom: 2rem;
}
</style>

