<template>
  <section class="register-section py-5">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-md-5">
          <div class="card shadow-sm p-4">
            <h2 class="text-center mb-4">Регистрация</h2>
            <form @submit.prevent="register">
              <div class="mb-3">
                <label class="form-label">Имя</label>
                <input type="text" class="form-control" v-model="user.name" placeholder="Введите имя" required>
              </div>
              <div class="mb-3">
                <label class="form-label">E-mail</label>
                <input type="email" class="form-control" v-model="user.email" placeholder="Введите e-mail" required>
              </div>
              <div class="mb-3">
                <label class="form-label">Телефон</label>
                <input type="text" class="form-control" v-model="user.phone" placeholder="Введите телефон" required>
              </div>
              <div class="mb-3">
                <label class="form-label">Пароль</label>
                <input type="password" class="form-control" v-model="user.password" placeholder="Введите пароль" required>
              </div>
              <div class="mb-3">
                <label class="form-label">Подтверждение пароля</label>
                <input type="password" class="form-control" v-model="user.passwordConfirm" placeholder="Подтвердите пароль" required>
              </div>
              <button type="submit" class="btn btn-primary w-100">Зарегистрироваться</button>
            </form>
            <p class="text-center mt-3">
              Уже есть аккаунт? 
              <router-link class="text-primary" to="/login">Войти</router-link>
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

const user = ref({
  name: '',
  email: '',
  phone: '',
  password: '',
  passwordConfirm: ''
});

function register() {
  if (!user.value.name || !user.value.email || !user.value.phone || !user.value.password || !user.value.passwordConfirm) {
    alert('Пожалуйста, заполните все поля!');
    return;
  }

  if (user.value.password !== user.value.passwordConfirm) {
    alert('Пароли не совпадают!');
    return;
  }

}
</script>

<style scoped>
.register-section {
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
