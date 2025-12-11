<template>
  <div class="row g-4 mb-5">
    <div class="col-md-4" v-for="car in cars" :key="car.id">
      <div class="card h-100 shadow-sm">
        <img :src="car.image" class="card-img-top" :alt="car.name" style="height:200px; object-fit:cover;">
        <div class="card-body d-flex flex-column">
          <h5 class="card-title">{{ car.name }}</h5>
          <p class="card-text text-muted">{{ car.description }}</p>
          <div class="mt-auto d-flex justify-content-between align-items-center">
            <span class="fw-bold">{{ car.price }} ₸/день</span>
            <button class="btn btn-primary btn-sm">Арендовать</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

defineProps({
  cars: Array
});
</script>
