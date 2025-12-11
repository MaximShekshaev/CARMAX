<template>
  <div class="d-flex flex-column min-vh-100">

    <Header />

    <main class="flex-fill">
      <!-- Страницы / контент -->
      <Home></Home>
    </main>

    <footer class="bg-dark text-light py-3 mt-auto">
      <Footer />
    </footer>

  </div>
     

</template>

<script setup>
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'

import Home from './pages/Home.vue';
</script>
