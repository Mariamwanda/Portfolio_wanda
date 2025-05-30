<script setup>
import Navbar from './layouts/Navbar.vue'
import Footer from './layouts/Footer.vue'
</script>

<template>
  <div class="app-container">
    <Navbar />
    <main class="main-content">
      <router-view></router-view>
    </main>
    <Footer />
  </div>
</template>

<style>
:root {
  --primary-color: #42b983;
  --text-color: #2c3e50;
  --bg-color: #ffffff;
  --navbar-height: 70px;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  overflow-x: hidden;
  height: 100%;
}

body {
  margin: 0;
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: var(--text-color);
  background-color: var(--bg-color);
  min-height: 100vh;
  overflow-x: hidden;
}

#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  position: relative;
  overflow-x: hidden;
}

.app-container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  width: 100%;
  position: relative;
}

.main-content {
  flex: 1;
  margin-top: var(--navbar-height);
  width: 100%;
  position: relative;
  z-index: 1;
  display: flex;
  flex-direction: column;
  overflow-x: hidden;
  padding: 0;
  margin-left: 0;
  margin-right: 0;
}

@media (max-width: 1440px) {
  .main-content {
    width: 100%;
  }
}

@media (max-width: 768px) {
  :root {
    --navbar-height: 60px;
  }

  .main-content {
    padding: 1rem;
  }
}
</style>
