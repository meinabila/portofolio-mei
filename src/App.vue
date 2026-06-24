<script setup>
import { ref } from 'vue'

import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Education from './components/Education.vue'
import Skills from './components/Skills.vue'
import Projects from './components/Projects.vue'
import Certificate from './components/Certificate.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'

const darkMode = ref(false)

const toggleDarkMode = () => {
  darkMode.value = !darkMode.value
}
</script>

<template>
  <div :class="{ darkMode: darkMode }">

    <Navbar />

    <div class="container">
      <Hero />
      <About />
      <Education />
      <Skills />
      <Projects />
      <Certificate />
      <Contact />
      <Footer />
    </div>

    <button class="theme-btn" @click="toggleDarkMode">
      {{ darkMode ? '☀️' : '🌙' }}
    </button>

  </div>
</template>

<style>
html,
body,
#app{
  margin:0;
  padding:0;
  min-height:100vh;
}

/* Tombol Dark Mode */
.theme-btn{
  position:fixed;
  bottom:25px;
  right:25px;
  width:60px;
  height:60px;
  border:none;
  border-radius:50%;
  background:#ff1493;
  color:white;
  font-size:24px;
  cursor:pointer;
  z-index:9999;
  box-shadow:0 8px 20px rgba(255,20,147,.35);
  transition:.3s;
}

.theme-btn:hover{
  transform:scale(1.08);
}

/* DARK MODE */
.darkMode{
  background:linear-gradient(
    135deg,
    #0f172a,
    #1e1b4b,
    #312e81
  );
  min-height:100vh;
}

/* Navbar */
.darkMode .navbar{
  background:#111827 !important;
}

.darkMode .logo,
.darkMode .nav-menu a{
  color:white !important;
}

/* Semua teks */
.darkMode h1,
.darkMode h2,
.darkMode h3,
.darkMode h4,
.darkMode p,
.darkMode span,
.darkMode li,
.darkMode a{
  color:white !important;
}

/* Card */
.darkMode .about-card,
.darkMode .info-card,
.darkMode .education-card,
.darkMode .stat-card,
.darkMode .skill-card,
.darkMode .project-card,
.darkMode .certificate-card,
.darkMode .contact-item,
.darkMode .profile-card{
  background:rgba(255,255,255,.08) !important;
  backdrop-filter:blur(15px);
  border:1px solid rgba(255,255,255,.1);
  color:white;
}

/* Teks abu */
.darkMode .hero-left p,
.darkMode .desc,
.darkMode .contact-subtitle,
.darkMode .profile-wrapper p,
.darkMode .info-item p{
  color:#d1d5db !important;
}

/* Tag Hero */
.darkMode .tag{
  background:rgba(255,255,255,.1);
  color:white;
}

/* Tahun Pendidikan */
.darkMode .education-year{
  background:rgba(255,20,147,.15);
}

/* Footer */
.darkMode footer{
  color:white;
}
</style>