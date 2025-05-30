<template>
  <div class="min-h-screen bg-gradient-to-b from-gray-50 to-white">
    <!-- Hero Section -->
    <section class="relative overflow-hidden">
      <!-- Fond décoratif -->
      <div class="absolute inset-0 bg-gradient-to-br from-primary/5 to-transparent">
        <div class="absolute inset-0 opacity-30">
          <div class="absolute top-0 left-0 w-96 h-96 bg-primary/10 rounded-full filter blur-3xl transform -translate-x-1/2 -translate-y-1/2"></div>
          <div class="absolute bottom-0 right-0 w-96 h-96 bg-blue-500/10 rounded-full filter blur-3xl transform translate-x-1/2 translate-y-1/2"></div>
        </div>
      </div>

      <!-- Contenu principal -->
      <div class="container mx-auto px-4 py-24 lg:py-32 relative z-10">
        <div class="flex flex-col items-center justify-center text-center">
          <div class="max-w-4xl">
            <p class="text-primary font-medium mb-4 tracking-wide uppercase text-sm">Bonjour, je suis</p>
            <h1 class="text-5xl lg:text-7xl font-bold text-gray-900 mb-6 leading-tight">
              Wandaogo Mariam
            </h1>
            <p class="text-2xl lg:text-3xl text-gray-600 mb-8 font-light">Développeur Front-end</p>
            <p class="text-lg text-gray-600 mb-12 max-w-2xl mx-auto leading-relaxed">
              Spécialisée dans le développement d'applications web et mobiles modernes avec React, React Native, Vue.js, Angular et JavaScript.
            </p>
          </div>

          <div class="flex flex-col sm:flex-row gap-6 mb-16">
            <router-link 
              to="/projects" 
              class="px-8 py-3 bg-primary text-white rounded-lg font-medium hover:bg-primary/90 transform hover:-translate-y-1 transition-all duration-300 shadow-lg hover:shadow-xl"
            >
              Voir mes projets
            </router-link>
            <router-link 
              to="/contact" 
              class="px-8 py-3 bg-white text-gray-800 rounded-lg font-medium hover:bg-gray-50 transform hover:-translate-y-1 transition-all duration-300 shadow-lg hover:shadow-xl border border-gray-100"
            >
              Me contacter
            </router-link>
          </div>

          <div class="flex flex-col items-center space-y-6">
            <span class="text-gray-500 font-medium">Technologies</span>
            <div class="flex gap-8 text-4xl text-gray-400">
              <i class="fab fa-react transform hover:scale-110 hover:text-primary transition-all duration-300 cursor-pointer" title="React"></i>
              <i class="fab fa-vuejs transform hover:scale-110 hover:text-primary transition-all duration-300 cursor-pointer" title="Vue.js"></i>
              <i class="fab fa-angular transform hover:scale-110 hover:text-primary transition-all duration-300 cursor-pointer" title="Angular"></i>
              <i class="fab fa-js transform hover:scale-110 hover:text-primary transition-all duration-300 cursor-pointer" title="JavaScript"></i>
            </div>
          </div>
        </div>
      </div>

      <!-- Décoration du bas -->
      <div class="absolute bottom-0 left-0 right-0 h-32 bg-gradient-to-t from-white to-transparent"></div>
    </section>

    <!-- Featured Projects Section -->
    <section class="py-24 bg-white relative overflow-hidden">
      <div class="container mx-auto px-4">
        <div class="text-center mb-16">
          <h2 class="text-4xl lg:text-5xl font-bold text-gray-900 mb-6">Projets récents</h2>
          <p class="text-lg text-gray-600 max-w-2xl mx-auto">Découvrez mes dernières réalisations en développement web</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-16">
          <div v-for="i in 3" :key="i" class="group bg-white rounded-2xl shadow-lg hover:shadow-xl transition-all duration-300 hover:-translate-y-1 overflow-hidden">
            <div class="h-48 bg-gray-100 relative overflow-hidden">
              <div class="absolute inset-0 bg-gradient-to-br from-gray-100 to-gray-200"></div>
            </div>
            <div class="p-6">
              <h3 class="text-xl font-semibold text-gray-900 mb-3">Projet {{i}}</h3>
              <p class="text-gray-600 mb-4">Description courte du projet avec les technologies utilisées.</p>
              <div class="flex flex-wrap gap-2">
                <span class="px-3 py-1 text-sm bg-primary/10 text-primary rounded-full">Vue.js</span>
                <span class="px-3 py-1 text-sm bg-primary/10 text-primary rounded-full">Node.js</span>
                <span class="px-3 py-1 text-sm bg-primary/10 text-primary rounded-full">MongoDB</span>
              </div>
            </div>
          </div>
        </div>

        <div class="text-center">
          <router-link 
            to="/projects" 
            class="inline-block px-8 py-3 border-2 border-primary text-primary font-medium rounded-lg hover:bg-primary hover:text-white transition-all duration-300 transform hover:-translate-y-1"
          >
            Voir tous les projets
          </router-link>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section class="py-24 bg-gray-50/50 relative overflow-hidden">
      <!-- Fond décoratif -->
      <div class="absolute inset-0">
        <div class="absolute top-0 right-0 w-96 h-96 bg-primary/5 rounded-full filter blur-3xl transform translate-x-1/2 -translate-y-1/2"></div>
        <div class="absolute bottom-0 left-0 w-96 h-96 bg-blue-500/5 rounded-full filter blur-3xl transform -translate-x-1/2 translate-y-1/2"></div>
      </div>

      <div class="container mx-auto px-4 relative z-10">
        <div class="text-center mb-20">
          <h2 class="text-4xl lg:text-5xl font-bold text-gray-900 mb-6">Compétences</h2>
          <p class="text-lg text-gray-600 max-w-2xl mx-auto">Expertise dans les technologies front-end modernes pour créer des expériences utilisateur exceptionnelles</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          <div class="group bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-all duration-300 hover:-translate-y-1">
            <div class="text-5xl text-primary mb-6 flex justify-center transform group-hover:scale-110 transition-transform duration-300">
              <i class="fab fa-react"></i>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-4 text-center">React & React Native</h3>
            <p class="text-gray-600 text-center leading-relaxed">Développement d'applications web et mobiles performantes</p>
          </div>

          <div class="group bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-all duration-300 hover:-translate-y-1">
            <div class="text-5xl text-primary mb-6 flex justify-center transform group-hover:scale-110 transition-transform duration-300">
              <i class="fab fa-vuejs"></i>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-4 text-center">Vue.js</h3>
            <p class="text-gray-600 text-center leading-relaxed">Création d'interfaces utilisateur modernes et réactives</p>
          </div>

          <div class="group bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-all duration-300 hover:-translate-y-1">
            <div class="text-5xl text-primary mb-6 flex justify-center transform group-hover:scale-110 transition-transform duration-300">
              <i class="fab fa-angular"></i>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-4 text-center">Angular</h3>
            <p class="text-gray-600 text-center leading-relaxed">Développement d'applications web robustes et évolutives</p>
          </div>

          <div class="group bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-all duration-300 hover:-translate-y-1">
            <div class="text-5xl text-primary mb-6 flex justify-center transform group-hover:scale-110 transition-transform duration-300">
              <i class="fab fa-js"></i>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-4 text-center">JavaScript</h3>
            <p class="text-gray-600 text-center leading-relaxed">Maîtrise du langage et de ses frameworks modernes</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section class="py-24 bg-gray-50/50 relative overflow-hidden">
      <!-- Fond décoratif -->
      <div class="absolute inset-0">
        <div class="absolute bottom-0 right-0 w-96 h-96 bg-primary/5 rounded-full filter blur-3xl transform translate-x-1/2 translate-y-1/2"></div>
        <div class="absolute top-0 left-0 w-96 h-96 bg-blue-500/5 rounded-full filter blur-3xl transform -translate-x-1/2 -translate-y-1/2"></div>
      </div>

      <div class="container mx-auto px-4 relative z-10">
        <div class="text-center mb-16">
          <h2 class="text-4xl lg:text-5xl font-bold text-gray-900 mb-6">Me Contacter</h2>
          <p class="text-lg text-gray-600 max-w-2xl mx-auto">Discutons de votre projet et voyons comment je peux vous aider</p>
        </div>

        <div class="max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-8">
          <!-- Informations de contact -->
          <div class="space-y-6">
            <div class="flex items-center space-x-4">
              <div class="w-12 h-12 bg-primary/10 rounded-lg flex items-center justify-center">
                <i class="fas fa-envelope text-primary text-xl"></i>
              </div>
              <div>
                <h3 class="text-lg font-semibold text-gray-900">Email</h3>
                <p class="text-gray-600">contact@example.com</p>
              </div>
            </div>

            <div class="flex items-center space-x-4">
              <div class="w-12 h-12 bg-primary/10 rounded-lg flex items-center justify-center">
                <i class="fas fa-phone text-primary text-xl"></i>
              </div>
              <div>
                <h3 class="text-lg font-semibold text-gray-900">Téléphone</h3>
                <p class="text-gray-600">+226 XX XX XX XX</p>
              </div>
            </div>

            <div class="flex items-center space-x-4">
              <div class="w-12 h-12 bg-primary/10 rounded-lg flex items-center justify-center">
                <i class="fas fa-map-marker-alt text-primary text-xl"></i>
              </div>
              <div>
                <h3 class="text-lg font-semibold text-gray-900">Localisation</h3>
                <p class="text-gray-600">Ouagadougou, Burkina Faso</p>
              </div>
            </div>
          </div>

          <!-- Formulaire de contact -->
          <div class="bg-white p-8 rounded-2xl shadow-lg">
            <form class="space-y-6">
              <div>
                <label for="name" class="block text-sm font-medium text-gray-700 mb-2">Nom complet</label>
                <input type="text" id="name" name="name" class="w-full px-4 py-3 rounded-lg border border-gray-200 focus:ring-2 focus:ring-primary focus:border-transparent outline-none transition-all duration-200" placeholder="Votre nom">
              </div>

              <div>
                <label for="email" class="block text-sm font-medium text-gray-700 mb-2">Email</label>
                <input type="email" id="email" name="email" class="w-full px-4 py-3 rounded-lg border border-gray-200 focus:ring-2 focus:ring-primary focus:border-transparent outline-none transition-all duration-200" placeholder="votre@email.com">
              </div>

              <div>
                <label for="message" class="block text-sm font-medium text-gray-700 mb-2">Message</label>
                <textarea id="message" name="message" rows="4" class="w-full px-4 py-3 rounded-lg border border-gray-200 focus:ring-2 focus:ring-primary focus:border-transparent outline-none transition-all duration-200" placeholder="Votre message"></textarea>
              </div>

              <button type="submit" class="w-full bg-primary text-white font-medium py-3 px-6 rounded-lg hover:bg-primary/90 transform hover:-translate-y-1 transition-all duration-300 shadow-lg hover:shadow-xl">
                Envoyer le message
              </button>
            </form>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
// Composition API
</script>

<style scoped>


/* Hero Section */
.hero {
  min-height: calc(100vh - var(--navbar-height));
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 4rem 2rem;
  background: linear-gradient(135deg, #111827 0%, #1f2937 100%);
  position: relative;
  width: 100%;
}

.hero-content {
  flex: 1;
  max-width: 800px;
  position: relative;
  z-index: 1;
  margin: 0 auto;
</style>
