<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-top">
        <div class="footer-brand">
          <div class="brand-info">
            <span class="brand-text">MW<span class="brand-dot">.</span></span>
            <p class="brand-desc">Développeur Full Stack Passionné</p>
          </div>
          <div class="social-links">
            <a href="#" target="_blank" class="social-link" title="GitHub">
              <i class="fab fa-github"></i>
            </a>
            <a href="#" target="_blank" class="social-link" title="LinkedIn">
              <i class="fab fa-linkedin-in"></i>
            </a>
            <a href="#" target="_blank" class="social-link" title="Twitter">
              <i class="fab fa-twitter"></i>
            </a>
          </div>
        </div>
        <nav class="footer-nav">
          <div class="nav-group">
            <h3>Navigation</h3>
            <ul>
              <li><router-link to="/">Accueil</router-link></li>
              <li><router-link to="/about">À propos</router-link></li>
              <li><router-link to="/projects">Projets</router-link></li>
              <li><router-link to="/contact">Contact</router-link></li>
            </ul>
          </div>
          <div class="nav-group">
            <h3>Services</h3>
            <ul>
              <li><a href="#">Web Design</a></li>
              <li><a href="#">Développement</a></li>
              <li><a href="#">UI/UX Design</a></li>
              <li><a href="#">Mobile Apps</a></li>
            </ul>
          </div>
        </nav>
      </div>
      <div class="footer-bottom">
        <p class="copyright">&copy; {{ currentYear }} MW. Tous droits réservés</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { computed } from 'vue'

const currentYear = computed(() => new Date().getFullYear())
</script>

<style scoped>
.footer {
  background-color: #111827;
  color: #fff;
  padding: 4rem 2rem 2rem;
  margin-top: auto;
  position: relative;
  border-top: 1px solid rgba(66, 185, 131, 0.3);
  width: 100%;
  box-sizing: border-box;
}

.footer::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 2px;
  background: linear-gradient(90deg, transparent, #42b983, transparent);
}

.footer-content {
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
}

.footer-top {
  display: flex;
  justify-content: space-between;
  gap: 4rem;
  margin-bottom: 3rem;
  flex-wrap: wrap;
}

.footer-brand {
  flex: 1;
  min-width: 300px;
  max-width: 400px;
}

.brand-info {
  margin-bottom: 2rem;
}

.brand-text {
  font-size: 3rem;
  font-weight: 800;
  letter-spacing: -1px;
  background: linear-gradient(135deg, #fff 0%, #42b983 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  display: inline-block;
}

.brand-dot {
  color: #42b983;
  -webkit-text-fill-color: #42b983;
}

.brand-desc {
  color: #9CA3AF;
  font-size: 1.1rem;
  line-height: 1.6;
  margin-top: 1rem;
  max-width: 400px;
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social-link {
  color: #9CA3AF;
  font-size: 1.2rem;
  transition: all 0.3s ease;
  padding: 0.6rem;
  border-radius: 8px;
  background: rgba(255, 255, 255, 0.05);
  display: flex;
  align-items: center;
  justify-content: center;
}

.social-link:hover {
  color: #42b983;
  background: rgba(66, 185, 131, 0.1);
  transform: translateY(-3px);
  box-shadow: 0 4px 12px rgba(66, 185, 131, 0.2);
}

.footer-nav {
  flex: 1;
  display: flex;
  justify-content: flex-end;
  gap: 4rem;
  padding-top: 1rem;
  min-width: 300px;
}

.nav-group {
  min-width: 160px;
}

.nav-group h3 {
  color: #42b983;
  font-size: 0.875rem;
  font-weight: 600;
  margin-bottom: 1.25rem;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.nav-group ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.nav-group li {
  margin-bottom: 0.75rem;
}

.nav-group a {
  color: #9CA3AF;
  text-decoration: none;
  font-size: 0.95rem;
  transition: all 0.3s ease;
  display: inline-block;
  padding: 0.25rem 0;
  position: relative;
}

.nav-group a::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 1px;
  background-color: #42b983;
  transition: width 0.3s ease;
}

.nav-group a:hover {
  color: #42b983;
}

.nav-group a:hover::after {
  width: 100%;
}

.footer-bottom {
  padding-top: 1.5rem;
  margin-top: 1.5rem;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  text-align: center;
}

.copyright {
  color: #6B7280;
  font-size: 0.875rem;
}

@media (max-width: 1200px) {
  .footer-content {
    max-width: 1200px;
  }
}

@media (max-width: 992px) {
  .footer-nav {
    gap: 2rem;
  }

  .footer-top {
    gap: 3rem;
  }
}

@media (max-width: 768px) {
  .footer {
    padding: 3rem 1.5rem 1.5rem;
  }

  .footer-top {
    flex-direction: column;
    gap: 2rem;
  }

  .footer-brand {
    max-width: 100%;
  }

  .footer-nav {
    justify-content: space-between;
    width: 100%;
    padding-top: 2rem;
  }

  .brand-text {
    font-size: 2.5rem;
  }

  .brand-desc {
    max-width: 100%;
  }

  .nav-group {
    min-width: 120px;
  }
}

@media (max-width: 576px) {
  .footer-nav {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 2rem;
  }

  .nav-group {
    min-width: 100%;
  }

  .social-links {
    justify-content: center;
  }

  .footer-brand {
    text-align: center;
  }

  .brand-desc {
    margin: 1rem auto;
  }
}
</style>
