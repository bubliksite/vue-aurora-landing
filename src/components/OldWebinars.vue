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
          name: 'Экспресс-аудит для выявления проблем и генерации решений задач',
          speaker: 'Алексей Калачев',
          date: '11 марта 2021 г.',
          time: '19:00',
          download:
                  'https://firebasestorage.googleapis.com/v0/b/korablikstorage.appspot.com/o/AuroraCons%2F%D0%92%D0%B5%D0%B1%D0%B8%D0%BD%D0%B0%D1%80_%D0%90%D1%83%D0%B4%D0%B8%D1%82_%D0%BF%D1%80%D0%BE%D0%B1%D0%BB%D0%B5%D0%BC%D1%8B_%D0%B8_%D1%80%D0%B5%D1%88%D0%B5%D0%BD%D0%B8%D1%8F_2021_03_11_%D0%90%D0%9A.pdf?alt=media&token=5191c18f-847e-46d8-b38d-96ff31fbe7b6'

        },
        {
          name: 'Проектный подход к решению нетривиальных задач',
          speaker: 'Вадим Витальевич Чухлебов',
          date: '24 февраля 2021 г.',
          time: '19:00',
          download:
            'https://firebasestorage.googleapis.com/v0/b/korablikstorage.appspot.com/o/AuroraCons%2FProektnyi_podhod_k_netrivialnym_zadacham_24022021.pdf?alt=media&token=e7b9d850-09a7-42ce-b770-acd2152cb120'
        },

      ]
    })
  }
</script>

<style scoped></style>
