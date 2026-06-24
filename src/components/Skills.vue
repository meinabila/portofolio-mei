<script setup>
const skills = [
  { icon: '🌐', name: 'HTML' },
  { icon: '🎨', name: 'CSS' },
  { icon: '⚡', name: 'JavaScript' },
  { icon: '💚', name: 'Vue.js' },
  { icon: '☕', name: 'Java' },
  { icon: '🗄️', name: 'MySQL' }
]
</script>

<template>
  <section id="skills" class="section">

    <h2 class="section-title">
      Skills
    </h2>

    <div class="skills-grid">

      <div
        v-for="skill in skills"
        :key="skill.name"
        class="skill-card"
      >

        <div class="skill-icon">
          {{ skill.icon }}
        </div>

        <h3>
          {{ skill.name }}
        </h3>

      </div>

    </div>

  </section>
</template>