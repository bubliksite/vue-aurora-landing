<template>
  <section class="my-5">
    <div class="container">
      <h3 class="text-red text-center mb-5 pb-3">
        Материалы прошедших вебинаров
      </h3>
      <div
        class="row mt-3 pb-5"
        v-for="archive in archives"
        :key="archive.name"
      >
        <div class="col-lg-3 col-md-6 col-12 mb-3">
          <p class="lead">
            {{ archive.date }} <br />
            {{ archive.time }}
          </p>
        </div>
        <div class="col-lg-9 col-md-6 col-12">
          <p class="text-red m-0">{{ archive.speaker }}</p>
          <p class="font-weight-bolder text-blue lead">
            {{ archive.name }}
          </p>

          <a :href="archive.download" download class="text-blue small">
            Скачать материалы
          </a>
        </div>
      </div>
    </div>
    <hr />
  </section>
</template>

<script>
  export default {
    name: 'OldWebinars',
    data: () => ({
      archives: [
        {
          name: 'Проектный подход к решению нетривиальных задач',
          speaker: 'Вадим Витальевич Чухлебов',
          date: '24 февраля 2021 г.',
          time: '19:00',
          download:
            'https://firebasestorage.googleapis.com/v0/b/korablikstorage.appspot.com/o/AuroraCons%2FProektnyi_podhod_k_netrivialnym_zadacham_24022021.pdf?alt=media&token=e7b9d850-09a7-42ce-b770-acd2152cb120'
        }
      ]
    })
  }
</script>

<style scoped></style>
