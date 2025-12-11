<template>
  <section class="conditions-section py-5">
    <h2 class="text-center mb-5">Условия</h2>
    <div class="row g-4 justify-content-center text-center">
      <div class="col-md-3" v-for="condition in conditions" :key="condition.title">
        <i :class="condition.icon + ' fs-1 mb-2'"></i>
        <h5>{{ condition.title }}</h5>
        <p>{{ condition.description }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import { defineProps } from 'vue';

defineProps({
  conditions: Array
});
</script>
