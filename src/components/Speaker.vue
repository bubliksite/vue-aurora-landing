<template>
  <section class="my-3 py-5" id="speaker">
    <div class="container">
      <div class="row">
        <div class="col-md-4 col-12 mb-3">
          <img
            class="w-100"
            src="@/assets/img/photo_2020-11-11_15-01-02.jpg"
            alt=""
          />
        </div>
        <div class="col-md-8 col-12 pl-lg-5">
          <h2 class="text-blue">Спикер</h2>
          <p class="font-weight-bolder text-red mt-3">Алексей Калачев</p>
          <p>
            Эксперт-практик по управлению изменениями и построению эффективной
            системы управления.
          </p>
          <p>
            Более 20 лет управленческого опыта, 11 профессиональных премий (в
            т.ч. Ассоциации директоров по коммуникациям России), десятки
            проектов и бизнесы, которые из региональных выросли в топ-25
            компаний мира в своей отрасли.
          </p>
          <a href="//auroracons.io" target="_blank" class=""
            >Подробнее о спикере</a
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'Speaker'
  }
</script>

<style scoped>
  a {
    color: #59607a;
    text-decoration: underline;
  }
  img {
    object-fit: cover;
    height: 100%;
  }
</style>
