<template>
  <nav class="navbar" :class="{ 'scrolled': isScrolled }">
    <div class="nav-brand">
      <router-link to="/">
        <span class="brand-text">MW</span>
        <span class="brand-dot">.</span>
      </router-link>
    </div>
    <div class="nav-links">
      <router-link to="/" class="nav-link" exact-active-class="active">Accueil</router-link>
      <router-link to="/about" class="nav-link" active-class="active">À propos</router-link>
      <router-link to="/projects" class="nav-link" active-class="active">Projets</router-link>
      <router-link to="/contact" class="nav-link" active-class="active">Contact</router-link>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 20
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 70px;
  background-color: rgba(0, 0, 0, 0.1);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 4rem;
  transition: all 0.3s ease;
  z-index: 1000;
  backdrop-filter: blur(10px);
}

.scrolled {
  height: 60px;
  box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
  background-color: rgba(255, 255, 255, 0.98);
}

.nav-brand a {
  text-decoration: none;
  display: flex;
  align-items: center;
}

.brand-text {
  color: #2c3e50;
  font-size: 1.8rem;
  font-weight: 700;
  letter-spacing: -1px;
}

.brand-dot {
  color: #42b983;
  font-size: 2.2rem;
  font-weight: 700;
  margin-left: -2px;
}

.nav-links {
  display: flex;
  gap: 2.5rem;
}

.nav-link {
  color: #2c3e50;
  text-decoration: none;
  font-size: 1rem;
  font-weight: 500;
  padding: 0.5rem 0;
  position: relative;
  transition: color 0.3s ease;
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background-color: #42b983;
  transition: width 0.3s ease;
}

.nav-link:hover {
  color: #42b983;
}

.nav-link:hover::after,
.nav-link.active::after {
  width: 100%;
}

.nav-link.active {
  color: #42b983;
  font-weight: 600;
}

@media (max-width: 768px) {
  .navbar {
    padding: 0 1.5rem;
  }
  
  .nav-links {
    gap: 1.5rem;
  }
  
  .brand-text {
    font-size: 1.5rem;
  }
  
  .brand-dot {
    font-size: 1.8rem;
  }
}
</style>
