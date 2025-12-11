<template>
  <main class="flex-fill py-5 bg-light">
    <div class="container">
      <h1 class="mb-4 text-center">Аренда автомобилей</h1>
      <CarList :cars="cars" />
      <Conditions :conditions="conditions" />
      <Reviews :reviews="reviews" />
      <Contact />
    </div>
  </main>
</template>

<script setup>
import { ref } from 'vue';
import CarList from '../components/CarList.vue';
import Conditions from '../components/Conditions.vue';
import Reviews from '../components/Reviews.vue';
import Contact from '../components/Contact.vue';


// Автомобили
const cars = ref([
  { id: 1, name: 'Toyota Camry', description: 'Комфортный седан для города и путешествий', price: 15000, image: 'https://via.placeholder.com/400x250?text=Toyota+Camry' },
  { id: 2, name: 'BMW X5', description: 'Мощный внедорожник с полным приводом', price: 30000, image: 'https://via.placeholder.com/400x250?text=BMW+X5' },
  { id: 3, name: 'Hyundai Solaris', description: 'Экономичный и надёжный автомобиль', price: 12000, image: 'https://via.placeholder.com/400x250?text=Hyundai+Solaris' },
  { id: 4, name: 'Mercedes-Benz S-Class', description: 'Люкс авто для VIP-клиентов', price: 50000, image: 'https://via.placeholder.com/400x250?text=Mercedes+S' },
]);

// Условия
const conditions = ref([
  { icon: 'bi bi-clock-history', title: 'Круглосуточная поддержка', description: 'Мы работаем 24 часа, 7 дней в неделю без выходных' },
  { icon: 'bi bi-car-front', title: 'Личный автопарк', description: 'У нас вы найдете автомобили как эконом класса так и премиум класса' },
  { icon: 'bi bi-stopwatch', title: 'Быстрое оформление', description: 'Оформление документов займет 10 минут. Минимальный пакет документов' },
  { icon: 'bi bi-truck', title: 'Доставка авто', description: 'Доставим автомобиль в любую часть города' },
]);

// Отзывы
const reviews = ref([
  { id: 1, name: 'Алексей П.', avatar: 'https://via.placeholder.com/50', rating: 5, text: 'Отличная компания! Машины всегда в отличном состоянии, обслуживание на высшем уровне.' },
  { id: 2, name: 'Мария С.', avatar: 'https://via.placeholder.com/50', rating: 4, text: 'Быстро оформили аренду, персонал вежливый. Советую для поездок по городу.' },
  { id: 3, name: 'Игорь К.', avatar: 'https://via.placeholder.com/50', rating: 5, text: 'Очень удобный сервис. Машину доставили прямо к дому, всё прошло без проблем.' },
]);
</script>
