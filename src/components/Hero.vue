<script setup>
import { ref, onMounted } from 'vue'
import profileImg from '../assets/profil.jpeg'

const texts = [
  'Mei Nabila'
]

const typingText = ref('')

onMounted(() => {
  let textIndex = 0
  let charIndex = 0
  let deleting = false

  setInterval(() => {

    const currentText = texts[textIndex]

    if (!deleting) {

      typingText.value =
        currentText.slice(0, charIndex)

      charIndex++

      if (charIndex > currentText.length) {
        deleting = true
      }

    } else {

      typingText.value =
        currentText.slice(0, charIndex)

      charIndex--

      if (charIndex < 0) {
        deleting = false
        textIndex = (textIndex + 1) % texts.length
      }

    }

  }, 120)
})
</script>

<template>
  <section id="home" class="hero">

    <div class="hero-left">

      <span class="tag">
        🚀 Informatics Student
      </span>

      <h1>
  Hi, I'm
  <br>

  <span class="typing-text">
    {{ typingText }}
    <span class="cursor">|</span>
  </span>
</h1>

      <p>
     Mahasiswa Informatika yang sedang mempelajari
Data Engineering, Database Management,
dan analisis data sebagai bekal menuju karier
sebagai Data Engineer.
      </p>

      <a href="#about" class="btn-primary">
        Lihat Portofolio
      </a>

    </div>

    <div class="hero-right">

      <div class="profile-wrapper">

  <div class="profile-circle">

    <img
      :src="profileImg"
      alt="Profile">

  </div>

  <h2>Mei Nabila</h2>

  <p>Informatics Student</p>

</div>

    </div>

  </section>
</template>