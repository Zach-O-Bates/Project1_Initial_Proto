<template>
  <div class="app-container">
    <div class="content-card">
    

      <div class="small-rectangles">
        <div class="small-rectangle"></div>
        <div class="small-rectangle"></div>
        <div class="small-rectangle"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
body, html, #app {
  margin: 0;
  padding: 0;
  height: 100%;
}

/* Gradient Background */
.app-container {
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(to bottom, #1E1E1E, #251C53);
}

/* Centered Rectangle (Card) */
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

/* Container for small rectangles */
.small-rectangles {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  width: 100%;
  align-items: center;
  margin-top: 1rem;
}

/* Individual small rectangles */
.small-rectangle {
  width: 80%;
  height: 100px;
  background-color: #1E1E1E;
  border-radius: 0.5rem;
}
</style>

