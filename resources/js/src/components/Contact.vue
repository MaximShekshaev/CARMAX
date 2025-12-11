<template>
  <section class="contact-section py-5 mt-5">
    <h2 class="text-center mb-5">Есть вопросы или предложения? Свяжитесь с нами</h2>
    <div class="row justify-content-center">
      <div class="col-md-6 mb-4">
        <form>
          <div class="mb-3">
            <label class="form-label">Ваше имя</label>
            <input type="text" class="form-control"  placeholder="Введите ваше имя">
          </div>
          <div class="mb-3">
            <label class="form-label">Ваш телефон *</label>
            <input type="tel" class="form-control"  placeholder="+7 (___) ___-__-__" required>
          </div>
          <div class="mb-3">
            <label class="form-label">Текст сообщения</label>
            <textarea class="form-control" rows="4" placeholder="Введите ваше сообщение"></textarea>
          </div>
          <button type="submit" class="btn btn-primary">Отправить</button>
        </form>
      </div>
      <div class="col-md-4">
        <h5>Телефоны</h5>
        <p>+7 949-342-19-20</p>
        <p>+380 99-014-42-00</p>
        <p>+48 789-610-934</p>

      </div>
    </div>
  </section>
</template>

<script setup>

</script>
