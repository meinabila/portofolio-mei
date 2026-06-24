<script setup>
const projects = [
  {
    title: 'Portfolio Website',
    desc: 'Website portofolio modern menggunakan Vue 3.'
  },
  {
    title: 'Database System',
    desc: 'Perancangan database relasional menggunakan MySQL.'
  },
  {
    title: 'Dashboard Monitoring',
    desc: 'Dashboard visualisasi data modern.'
  }
]
</script>

<template>
  <section id="projects" class="section">

    <h2 class="section-title">
      Projects
    </h2>

    <div class="project-grid">

      <div
        v-for="project in projects"
        :key="project.title"
        class="project-card"
      >
        <h3>{{ project.title }}</h3>

        <p>
          {{ project.desc }}
        </p>
      </div>

    </div>

  </section>
</template>