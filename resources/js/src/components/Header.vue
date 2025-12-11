<template>
  <nav class="navbar navbar-expand bg-white shadow-sm py-3">
  <div class="container d-flex align-items-center justify-content-between">
    
    <!-- Лого -->
    <a class="navbar-brand fw-bold fs-3 text-primary" href="#">
      CAR<span class="text-dark">MAX</span>
    </a>

    <!-- Навигация -->
    <ul class="navbar-nav d-flex flex-row gap-4 fs-5">
      <li class="nav-item">
        <a class="nav-link text-dark hover-primary" href="/">Главная</a>
      </li>
      <li class="nav-item">
        <a class="nav-link text-dark hover-primary" href="/rent">Аренда</a>
      </li>
      <li class="nav-item">
        <a class="nav-link text-dark hover-primary" href="/my-rent">Моя аренда</a>
      </li>
      <li class="nav-item">
        <a class="nav-link text-dark hover-primary" href="/login">Вход</a>
      </li>
      <li class="nav-item">
        <a class="btn btn-primary px-3 py-2" href="/register">Регистрация</a>
      </li>
    </ul>

  </div>
</nav>
</template>

<script setup>
</script>

<style scoped>
header {
  position: sticky;
  top: 0;
  z-index: 50;
}
</style>

