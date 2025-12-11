<template>
  <div class="d-flex flex-column min-vh-100">
    <Header />

    <main class="flex-fill">
      <router-view /> <!-- сюда рендерятся все страницы -->
    </main>

    <Footer />
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
</script>
