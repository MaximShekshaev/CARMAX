<template>
  <section class="login-section py-5">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-md-5">
          <div class="card shadow-sm p-4">
            <h2 class="text-center mb-4">Вход в аккаунт</h2>
            <form @submit.prevent="login">
              <div class="mb-3">
                <label class="form-label">E-mail или телефон</label>
                <input type="text" class="form-control" v-model="credentials.user" placeholder="Введите e-mail или телефон" required>
              </div>
              <div class="mb-3">
                <label class="form-label">Пароль</label>
                <input type="password" class="form-control" v-model="credentials.password" placeholder="Введите пароль" required>
              </div>
              <button type="submit" class="btn btn-primary w-100">Войти</button>
            </form>
            <p class="text-center mt-3">
  Нет аккаунта? 
  <router-link to="/register" class="text-primary">Зарегистрироваться</router-link>
</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

const credentials = ref({
  user: '',
  password: ''
});

function login() {
  if (!credentials.value.user || !credentials.value.password) {
    alert('Пожалуйста, заполните все поля!');
    return;
  }
}

</script>

<style scoped>
.login-section {
  background-color: #f8f9fa;
  min-height: 80vh;
  display: flex;
  align-items: center;
}

.card {
  border-radius: 12px;
}

.card h2 {
  font-weight: 700;
}

.btn-primary {
  background-color: #0d6efd;
  border-color: #0d6efd;
}

.btn-primary:hover {
  background-color: #0b5ed7;
  border-color: #0a58ca;
}
</style>
