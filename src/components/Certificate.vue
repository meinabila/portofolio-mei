<script setup>
import sertifikat1 from '../assets/sertifikat.jpeg'
import sertifikat2 from '../assets/sertifikatco.jpeg'
import sertifikat3 from '../assets/sertifikatk.jpeg'

const certificates = [
  {
    title:'Dasar Pemrograman Web',
    image: sertifikat1
  },
  {
    title:'SDGs',
    image: sertifikat2
  },
  {
    title:'SDGs',
    image: sertifikat3
  }
]
</script>

<template>

<section id="certificate" class="section">

  <h2 class="section-title">
    Sertifikat
  </h2>

  <div class="certificate-grid">

    <div
      v-for="item in certificates"
      :key="item.title"
      class="certificate-card"
    >

      <img
        :src="item.image"
        :alt="item.title"
      >

      <h3>
        {{ item.title }}
      </h3>

    </div>

  </div>

</section>

</template>