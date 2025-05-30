<template>
  <div class="contact-page">
    <!-- En-tête -->
    <header class="contact-header">
      <div class="header-content">
        <h1 class="header-title">Contactez-moi</h1>
        <p class="header-subtitle">Discutons de votre projet</p>
      </div>
    </header>

    <!-- Section principale -->
    <section class="contact-section">
      <div class="container">
        <div class="contact-grid">
          <!-- Informations de contact -->
          <div class="contact-info">
            <h2>Informations de contact</h2>
            <p class="info-text">N'hésitez pas à me contacter pour toute question ou proposition de projet. Je vous répondrai dans les plus brefs délais.</p>
            
            <div class="info-items">
              <div class="info-item">
                <div class="info-icon">
                  <i class="fas fa-envelope"></i>
                </div>
                <div class="info-content">
                  <h3>Email</h3>
                  <p>mariamwandaogo7@gmail.com</p>
                </div>
              </div>

              <div class="info-item">
                <div class="info-icon">
                  <i class="fas fa-phone"></i>
                </div>
                <div class="info-content">
                  <h3>Téléphone</h3>
                  <p>05 75 53 05 18 / 07 87 61 64 96</p>
                </div>
              </div>

              <div class="info-item">
                <div class="info-icon">
                  <i class="fas fa-map-marker-alt"></i>
                </div>
                <div class="info-content">
                  <h3>Localisation</h3>
                  <p>Abidjan, Koumassi - Côte d'Ivoire</p>
                </div>
              </div>
            </div>

            <div class="social-links">
              <a href="#" class="social-link" title="LinkedIn" target="_blank" rel="noopener noreferrer">
                <i class="fab fa-linkedin"></i>
              </a>
              <a href="#" class="social-link" title="GitHub" target="_blank" rel="noopener noreferrer">
                <i class="fab fa-github"></i>
              </a>
              <a href="#" class="social-link" title="Facebook" target="_blank" rel="noopener noreferrer">
                <i class="fab fa-facebook"></i>
              </a>
            </div>
          </div>

          <!-- Formulaire de contact -->
          <div class="contact-form">
            <form @submit.prevent="handleSubmit">
              <div class="form-group">
                <label for="name">Nom complet</label>
                <input 
                  type="text" 
                  id="name" 
                  v-model="formData.name"
                  required
                  placeholder="Votre nom"
                >
              </div>

              <div class="form-group">
                <label for="email">Email</label>
                <input 
                  type="email" 
                  id="email" 
                  v-model="formData.email"
                  required
                  placeholder="votre@email.com"
                >
              </div>

              <div class="form-group">
                <label for="subject">Sujet</label>
                <input 
                  type="text" 
                  id="subject" 
                  v-model="formData.subject"
                  required
                  placeholder="Le sujet de votre message"
                >
              </div>

              <div class="form-group">
                <label for="message">Message</label>
                <textarea 
                  id="message" 
                  v-model="formData.message"
                  required
                  rows="6"
                  placeholder="Votre message"
                ></textarea>
              </div>

              <button type="submit" class="submit-btn">
                <span>Envoyer le message</span>
                <i class="fas fa-paper-plane"></i>
              </button>
            </form>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const formData = ref({
  name: '',
  email: '',
  subject: '',
  message: ''
})

const handleSubmit = () => {
  // Ici, implémenter la logique d'envoi du formulaire
  console.log('Formulaire soumis:', formData.value)
}
</script>

<style scoped>
.contact-page {
  background: #fff;
}

/* Header */
.contact-header {
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

/* Contact Section */
.contact-section {
  padding: 6rem 0;
}

.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: 4rem;
}

/* Contact Info */
.contact-info h2 {
  font-size: 2rem;
  color: #111827;
  margin-bottom: 1.5rem;
}

.info-text {
  color: #6B7280;
  line-height: 1.6;
  margin-bottom: 3rem;
}

.info-items {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  margin-bottom: 3rem;
}

.info-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
}

.info-icon {
  width: 40px;
  height: 40px;
  background: rgba(66, 185, 131, 0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.info-icon i {
  color: var(--primary-color);
  font-size: 1.2rem;
}

.info-content h3 {
  font-size: 1.1rem;
  color: #111827;
  margin-bottom: 0.5rem;
}

.info-content p {
  color: #6B7280;
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social-link {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: #f3f4f6;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #4B5563;
  transition: all 0.3s ease;
}

.social-link:hover {
  background: var(--primary-color);
  color: #fff;
  transform: translateY(-3px);
}

/* Contact Form */
.contact-form {
  background: #fff;
  padding: 2rem;
  border-radius: 1rem;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
}

.form-group {
  margin-bottom: 1.5rem;
}

label {
  display: block;
  font-size: 0.9rem;
  font-weight: 500;
  color: #374151;
  margin-bottom: 0.5rem;
}

input,
textarea {
  width: 100%;
  padding: 0.75rem 1rem;
  border: 1px solid #e5e7eb;
  border-radius: 0.5rem;
  background: #f9fafb;
  color: #111827;
  font-size: 1rem;
  transition: all 0.3s ease;
}

input:focus,
textarea:focus {
  outline: none;
  border-color: var(--primary-color);
  background: #fff;
  box-shadow: 0 0 0 3px rgba(66, 185, 131, 0.1);
}

.submit-btn {
  width: 100%;
  padding: 1rem;
  background: var(--primary-color);
  color: #fff;
  border: none;
  border-radius: 0.5rem;
  font-size: 1rem;
  font-weight: 600;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  cursor: pointer;
  transition: all 0.3s ease;
}

.submit-btn:hover {
  background: #3aa876;
  transform: translateY(-2px);
}

.submit-btn i {
  font-size: 1.1rem;
}

/* Responsive Design */
@media (max-width: 1024px) {
  .contact-section {
    padding: 4rem 0;
  }

  .contact-grid {
    gap: 3rem;
  }
}

@media (max-width: 768px) {
  .contact-grid {
    grid-template-columns: 1fr;
  }

  .header-title {
    font-size: 2.5rem;
  }

  .contact-info h2 {
    font-size: 1.75rem;
  }
}

@media (max-width: 480px) {
  .contact-header {
    padding: 4rem 1.5rem;
  }

  .container {
    padding: 0 1.5rem;
  }

  .header-title {
    font-size: 2rem;
  }

  .contact-form {
    padding: 1.5rem;
  }
}
</style>
