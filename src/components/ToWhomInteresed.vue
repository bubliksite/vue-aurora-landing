<template>
  <section class="my-5 py-3">
    <div class="container">
      <h2 class="text-red text-center mb-5 pb-3">Кому будет интересно?</h2>
      <div class="row">
        <div
          class="col-lg-3 col-md-6 col-12 mb-3"
          v-for="item in list"
          :key="item"
        >
          <div class="h-100 m-card py-5 px-4 d-flex align-items-center">
            <p class="m-0 text-center w-100">{{ item }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'ToWhomInteresed',
    data: () => ({
      list: [
        'Владельцы бизнесов',
        'Руководители организаций',
        'Руководители проектов',
        'Директора структурных подразделений'
      ],
      isShow: false
    })
  }
</script>

<style scoped></style>
