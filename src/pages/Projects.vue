<template>
  <div class="projects-page">
    <!-- En-tête -->
    <header class="projects-header">
      <div class="header-content">
        <h1 class="header-title">Mes Projets</h1>
        <p class="header-subtitle">Découvrez une sélection de mes réalisations</p>
      </div>
    </header>

    <!-- Filtres -->
    <section class="filters-section">
      <div class="container">
        <div class="filters">
          <button 
            v-for="filter in filters" 
            :key="filter"
            :class="['filter-btn', { active: currentFilter === filter }]"
            @click="currentFilter = filter"
          >
            {{ filter }}
          </button>
        </div>
      </div>
    </section>

    <!-- Grille de projets -->
    <section class="projects-grid">
      <div class="container">
        <div class="grid">
          <article 
            v-for="project in filteredProjects" 
            :key="project.id"
            class="project-card"
          >
            <div class="project-image">
              <img :src="project.image" :alt="project.title">
              <div class="project-overlay">
                <div class="project-links">
                  <a :href="project.demo" target="_blank" class="project-link">Voir le site</a>
                  <a :href="project.github" target="_blank" class="project-link">Code source</a>
                </div>
              </div>
            </div>
            <div class="project-info">
              <h3 class="project-title">{{ project.title }}</h3>
              <p class="project-description">{{ project.description }}</p>
              <div class="project-tech">
                <span v-for="tech in project.technologies" :key="tech" class="tech-tag">
                  {{ tech }}
                </span>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="cta-section">
      <div class="container">
        <h2>Vous avez un projet ?</h2>
        <p>Je suis disponible pour donner vie à vos idées</p>
        <router-link to="/contact" class="cta-button">Discutons-en</router-link>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'

// Filtres disponibles
const filters = ['Tous', 'Web', 'Mobile', 'UI/UX']
const currentFilter = ref('Tous')

// Données des projets
const projects = [
  {
    id: 1,
    title: 'E-commerce Modern',
    description: 'Une plateforme e-commerce moderne avec panier et paiement intégré',
    image: '/projects/ecommerce.jpg',
    demo: 'https://demo-ecommerce.com',
    github: 'https://github.com/username/ecommerce',
    technologies: ['Vue.js', 'Node.js', 'MongoDB'],
    category: 'Web'
  },
  {
    id: 2,
    title: 'Application Mobile Fitness',
    description: 'Application de suivi d\'entraînement et de nutrition',
    image: '/projects/fitness.jpg',
    demo: 'https://demo-fitness.com',
    github: 'https://github.com/username/fitness-app',
    technologies: ['React Native', 'Firebase'],
    category: 'Mobile'
  },
  {
    id: 3,
    title: 'Dashboard Analytics',
    description: 'Interface d\'administration avec visualisation de données',
    image: '/projects/dashboard.jpg',
    demo: 'https://demo-dashboard.com',
    github: 'https://github.com/username/dashboard',
    technologies: ['Vue.js', 'D3.js', 'Express'],
    category: 'Web'
  },
  {
    id: 4,
    title: 'Design System',
    description: 'Système de design complet pour applications web',
    image: '/projects/design.jpg',
    demo: 'https://demo-design.com',
    github: 'https://github.com/username/design-system',
    technologies: ['Figma', 'Storybook', 'React'],
    category: 'UI/UX'
  }
]

// Filtrage des projets
const filteredProjects = computed(() => {
  if (currentFilter.value === 'Tous') return projects
  return projects.filter(project => project.category === currentFilter.value)
})
</script>

<style scoped>
.projects-page {
  background: #fff;
}

/* Header */
.projects-header {
  background: linear-gradient(135deg, #111827 0%, #1f2937 100%);
  padding: 6rem 2rem;
  text-align: center;
  color: #fff;
}

.header-content {
  max-width: 800px;
  margin: 0 auto;
}

.header-title {
  font-size: 3rem;
  font-weight: 800;
  margin-bottom: 1rem;
  background: linear-gradient(135deg, #fff 0%, #42b983 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.header-subtitle {
  font-size: 1.25rem;
  color: #9CA3AF;
  line-height: 1.6;
}

/* Container */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

/* Filters */
.filters-section {
  padding: 2rem 0;
  background: #f9fafb;
  border-bottom: 1px solid #e5e7eb;
}

.filters {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}

.filter-btn {
  padding: 0.5rem 1rem;
  border: 1px solid #e5e7eb;
  border-radius: 9999px;
  background: #fff;
  color: #4B5563;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.3s ease;
}

.filter-btn:hover {
  border-color: var(--primary-color);
  color: var(--primary-color);
}

.filter-btn.active {
  background: var(--primary-color);
  color: #fff;
  border-color: var(--primary-color);
}

/* Projects Grid */
.projects-grid {
  padding: 4rem 0;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 2rem auto;
}
</style>
