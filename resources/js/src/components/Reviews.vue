<template>
  <section class="reviews-section py-5 mt-5">
    <h2 class="text-center mb-5">Отзывы наших клиентов</h2>
    <div class="row g-4 justify-content-center">
      <div class="col-md-4" v-for="review in reviews" :key="review.id">
        <div class="review-card p-4 h-100 shadow-sm">
          <div class="d-flex align-items-center mb-3">
            <img :src="review.avatar" alt="Avatar" class="rounded-circle me-3" style="width:50px; height:50px;">
            <div>
              <h5 class="mb-0">{{ review.name }}</h5>
              <div class="text-warning">
                <i class="bi bi-star-fill" v-for="n in review.rating" :key="n"></i>
              </div>
            </div>
          </div>
          <p class="mb-0">{{ review.text }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { defineProps } from 'vue';

defineProps({
  reviews: Array
});
</script>
