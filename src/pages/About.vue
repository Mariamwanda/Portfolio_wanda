<template>
  <div class="about">
    <!-- En-tête -->
    <header class="about-header">
      <div class="header-content">
        <h1 class="header-title">À propos de moi</h1>
        <p class="header-subtitle">Développeur passionné par la création d'expériences web innovantes</p>
      </div>
    </header>

    <!-- Section Présentation -->
    <section class="about-section presentation-section">
      <div class="section-content">
        <div class="text-content">
          <h2>Qui suis-je ?</h2>
          <p>Passionné par le développement web depuis plus de 5 ans, je crée des applications web modernes et performantes. Mon approche combine créativité et rigueur technique pour donner vie à des projets innovants.</p>
          <p>Je m'efforce constamment d'apprendre de nouvelles technologies et de me tenir à jour avec les dernières tendances du développement web.</p>
          <div class="stats">
            <div class="stat-item">
              <span class="stat-number">5+</span>
              <span class="stat-label">Années d'expérience</span>
            </div>
            <div class="stat-item">
              <span class="stat-number">50+</span>
              <span class="stat-label">Projets réalisés</span>
            </div>
            <div class="stat-item">
              <span class="stat-number">30+</span>
              <span class="stat-label">Clients satisfaits</span>
            </div>
          </div>
        </div>
        <div class="image-content">
          <div class="profile-image">
            <!-- Placeholder pour l'image de profil -->
            <div class="image-placeholder"></div>
          </div>
        </div>
      </div>
    </section>

    <!-- Section Parcours -->
    <section class="about-section journey-section">
      <div class="section-content">
        <h2>Mon parcours</h2>
        <div class="timeline">
          <div class="timeline-item">
            <div class="timeline-marker current"></div>
            <div class="timeline-content">
              <h3>Développeur Front-end - Stage</h3>
              <span class="timeline-date">Décembre 2024 - Présent</span>
              <p>Stage en développement Front-end chez RPCI (Hubgroupes). Spécialisation en React Native et Vue.js, Design: pour le développement d'applications web et mobiles modernes.</p>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-marker"></div>
            <div class="timeline-content">
              <h3>Licence en Développement d'Applications et E-services</h3>
              <span class="timeline-date">2024</span>
              <p>Formation en développement d'applications et services numériques à l'Université Virtuelle de Côte d'Ivoire (UVCI).</p>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-marker"></div>
            <div class="timeline-content">
              <h3>Formation à compléter</h3>
              <span class="timeline-date">2023 - 2024</span>
              <p>Description à venir...</p>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-marker"></div>
            <div class="timeline-content">
              <h3>Certification Développeur Front-end Javascript</h3>
              <span class="timeline-date">2023 - 2024</span>
              <p>Formation et certification en développement Front-end Javascript à NaN Digital Academy, spécialisation en développement d'applications web modernes.</p>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-marker"></div>
            <div class="timeline-content">
              <h3>Baccalauréat Série D</h3>
              <span class="timeline-date">2020 - 2021</span>
              <p>Obtention du Baccalauréat Série D au Lycée Municipal de Koumassi.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Section Valeurs -->
    <section class="about-section values-section">
      <div class="section-content">
        <h2>Mes valeurs</h2>
        <div class="values-grid">
          <div class="value-card">
            <div class="value-icon">
              <i class="fas fa-lightbulb"></i>
            </div>
            <h3>Innovation</h3>
            <p>Toujours à la recherche de nouvelles solutions et technologies pour améliorer les projets.</p>
          </div>
          <div class="value-card">
            <div class="value-icon">
              <i class="fas fa-users"></i>
            </div>
            <h3>Collaboration</h3>
            <p>Croire en la force du travail d'équipe et de la communication ouverte.</p>
          </div>
          <div class="value-card">
            <div class="value-icon">
              <i class="fas fa-rocket"></i>
            </div>
            <h3>Excellence</h3>
            <p>Viser la qualité dans chaque ligne de code et chaque interaction.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Section Contact -->
    <section class="about-section contact-section">
      <div class="section-content">
        <h2>Travaillons ensemble</h2>
        <p>Vous avez un projet intéressant ? Je serais ravi d'en discuter avec vous.</p>
        <div class="cta-buttons">
          <router-link to="/contact" class="btn btn-primary">Me contacter</router-link>
          <a href="#" class="btn btn-secondary">Télécharger CV</a>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
// Composition API
</script>

<style scoped>
.about-page {
  background: #fff;
  overflow: hidden;
  width: 100%;
  margin: 0;
  padding: 0;
}

/* Header */
.about-header {
  background: linear-gradient(135deg, #111827 0%, #1f2937 100%);
  padding: 4rem 0 2rem;
  text-align: center;
  color: #fff;
  position: relative;
  overflow: hidden;
  width: 100%;
  margin: 0;
  left: 0;
  right: 0;
}

.about-header::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml,<svg width="60" height="60" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg"><rect width="60" height="60" fill="none"/><path d="M12 0L24 12L12 24L0 12L12 0Z" fill="rgba(255,255,255,0.03)"/></svg>') repeat;
  opacity: 0.4;
}

.header-content {
  max-width: 1200px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
  padding: 0 2rem;
}

.header-title {
  font-size: 3.5rem;
  font-weight: 800;
  margin-bottom: 1.5rem;
  background: linear-gradient(135deg, #fff 0%, #42b983 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 0 2px 4px rgba(0,0,0,0.1);
  letter-spacing: -0.02em;
  animation: fadeInUp 0.6s ease-out;
}

.header-subtitle {
  font-size: 1.35rem;
  color: #9CA3AF;
  line-height: 1.6;
  max-width: 600px;
  margin: 0 auto;
  animation: fadeInUp 0.6s ease-out 0.2s both;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Sections */
.about-section {
  padding: 6rem 0;
  position: relative;
  overflow: hidden;
}

.about-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: linear-gradient(to right, transparent, rgba(66, 185, 131, 0.2), transparent);
}

.section-title {
  text-align: center;
  margin-bottom: 4rem;
  position: relative;
}

.section-title h2 {
  font-size: 2.5rem;
  color: #111827;
  font-weight: 800;
  margin-bottom: 1rem;
  background: linear-gradient(135deg, #111827 0%, #42b983 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.section-title::after {
  content: '';
  display: block;
  width: 80px;
  height: 4px;
  background: var(--primary-color);
  margin: 1rem auto 0;
  border-radius: 2px;
  box-shadow: 0 2px 4px rgba(66, 185, 131, 0.2);
}

/* Common Section Styles */
.about-section {
  padding: 6rem 2rem;
}

.section-content {
  max-width: 1200px;
  margin: 0 auto;
}

.section-content h2 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 3rem;
  color: #111827;
}

/* Presentation Section */
.presentation-section .section-content {
  display: grid;
  grid-template-columns: 3fr 2fr;
  gap: 4rem;
  align-items: center;
}

.text-content p {
  color: #4B5563;
  line-height: 1.8;
  margin-bottom: 1.5rem;
  font-size: 1.1rem;
}

.stats {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-top: 3rem;
}

.stat-item {
  text-align: center;
}

.stat-number {
  display: block;
  font-size: 2.5rem;
  font-weight: 700;
  color: var(--primary-color);
  margin-bottom: 0.5rem;
}

.stat-label {
  color: #6B7280;
  font-size: 0.9rem;
}

.profile-image {
  width: 100%;
  aspect-ratio: 1;
  border-radius: 1rem;
  overflow: hidden;
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
}

.image-placeholder {
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, #f3f4f6 0%, #e5e7eb 100%);
}

/* Journey Section */
.timeline {
  position: relative;
  padding-left: 2rem;
  max-width: 800px;
  margin: 0 auto;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  height: 100%;
  width: 3px;
  background: linear-gradient(to bottom, var(--primary-color) 0%, #e5e7eb 100%);
  border-radius: 4px;
}

.timeline-item {
  position: relative;
  margin-bottom: 3rem;
  opacity: 0.8;
  transform: translateX(20px);
  transition: all 0.3s ease;
}

.timeline-item:hover {
  opacity: 1;
  transform: translateX(0);
}

.timeline-marker {
  position: absolute;
  left: -8px;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  border: 3px solid var(--primary-color);
  background: #fff;
  margin-right: 1rem;
  flex-shrink: 0;
  transition: all 0.3s ease;
  z-index: 1;
}

.timeline-marker::before {
  content: '';
  position: absolute;
  top: 50%;
  left: 100%;
  width: 12px;
  height: 2px;
  background: var(--primary-color);
  transform: translateY(-50%);
}

.timeline-marker.current {
  background: var(--primary-color);
  box-shadow: 0 0 0 6px rgba(66, 185, 131, 0.2);
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0% {
    box-shadow: 0 0 0 0 rgba(66, 185, 131, 0.4);
  }
  70% {
    box-shadow: 0 0 0 10px rgba(66, 185, 131, 0);
  }
  100% {
    box-shadow: 0 0 0 0 rgba(66, 185, 131, 0);
  }
}

.timeline-content {
  background: #fff;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  transition: all 0.3s ease;
}

.timeline-content:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 12px -1px rgba(0, 0, 0, 0.1), 0 4px 6px -1px rgba(0, 0, 0, 0.06);
}

.timeline-content h3 {
  font-size: 1.25rem;
  color: #111827;
  margin-bottom: 0.5rem;
  font-weight: 600;
}

.timeline-date {
  font-size: 0.875rem;
  color: var(--primary-color);
  margin-bottom: 1rem;
  display: inline-block;
  padding: 0.25rem 0.75rem;
  background: rgba(66, 185, 131, 0.1);
  border-radius: 20px;
  font-weight: 500;
}

.timeline-content p {
  color: #4B5563;
  line-height: 1.6;
  margin: 0;
}

/* Values Section */
.values-section {
  background: #f9fafb;
}

.values-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2.5rem;
  margin-top: 3rem;
  padding: 0 2rem;
}

.value-card {
  background: #fff;
  padding: 2.5rem;
  border-radius: 16px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.value-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(to right, var(--primary-color), #42d392);
}

.value-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1.5rem;
}

.value-icon i {
  font-size: 1.5rem;
  color: var(--primary-color);
}

.value-card h3 {
  font-size: 1.25rem;
  color: #111827;
  margin-bottom: 1rem;
}

.value-card p {
  color: #6B7280;
  line-height: 1.6;
}

/* Contact Section */
.contact-section {
  text-align: center;
  background: linear-gradient(135deg, #111827 0%, #1f2937 100%);
  color: #fff;
}

.contact-section h2 {
  color: #fff;
}

.contact-section p {
  color: #9CA3AF;
  font-size: 1.1rem;
  margin-bottom: 2rem;
}

.cta-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
}

.btn {
  padding: 0.75rem 1.5rem;
  border-radius: 8px;
  font-weight: 600;
  text-decoration: none;
  transition: all 0.3s ease;
}

.btn-primary {
  background: var(--primary-color);
  color: #111827;
}

.btn-primary:hover {
  background: #3aa876;
  transform: translateY(-2px);
}

.btn-secondary {
  background: rgba(255, 255, 255, 0.1);
  color: #fff;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.btn-secondary:hover {
  background: rgba(255, 255, 255, 0.2);
  transform: translateY(-2px);
}

/* Animations */
@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(-30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInRight {
  from {
    opacity: 0;
    transform: translateX(30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes scaleIn {
  from {
    opacity: 0;
    transform: scale(0.9);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

/* Animation classes */
.animate-slide-left {
  animation: slideInLeft 0.6s ease-out both;
}

.animate-slide-right {
  animation: slideInRight 0.6s ease-out both;
}

.animate-scale {
  animation: scaleIn 0.6s ease-out both;
}

/* Animation delays */
.delay-1 { animation-delay: 0.1s; }
.delay-2 { animation-delay: 0.2s; }
.delay-3 { animation-delay: 0.3s; }
.delay-4 { animation-delay: 0.4s; }

/* Hover Effects */
.hover-lift {
  transition: transform 0.3s ease;
}

.hover-lift:hover {
  transform: translateY(-5px);
}

.hover-scale {
  transition: transform 0.3s ease;
}

.hover-scale:hover {
  transform: scale(1.02);
}

/* Responsive Design */
@media (max-width: 1024px) {
  .about-section {
    padding: 4rem 2rem;
  }

  .presentation-section .section-content {
    gap: 3rem;
  }

  .header-title {
    font-size: 2.5rem;
  }
}

@media (max-width: 768px) {
  .presentation-section .section-content {
    grid-template-columns: 1fr;
  }

  .stats {
    grid-template-columns: repeat(2, 1fr);
  }

  .section-content h2 {
    font-size: 2rem;
  }

  .timeline-item {
    padding-left: 2rem;
  }
}

@media (max-width: 480px) {
  .about-header {
    padding: 4rem 1.5rem;
  }

  .about-section {
    padding: 3rem 1.5rem;
  }

  .header-title {
    font-size: 2rem;
  }

  .stats {
    grid-template-columns: 1fr;
  }

  .cta-buttons {
    flex-direction: column;
  }

  .timeline-content h3 {
    font-size: 1.1rem;
  }
}
</style>
