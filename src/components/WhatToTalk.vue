<template>
  <section class="pt-5 pb-4 bg-dark" id="program">
    <div class="container pt-4">
      <h2 class="text-center text-white mb-5 pb-3">Что будем обсуждать?</h2>
      <div class="row my-3">
        <div
          class="col-md-4 col-12 mb-3 text-center h-100"
          v-for="item in cards"
          :key="item.description"
        >
          <img class="mb-4" :src="item.image" alt="" />
          <p class="d-flex align-items-center">
            <small class="text-white">{{ item.description }}</small>
          </p>
        </div>
      </div>
      <div class="d-flex justify-content-center w-100 mt-3 mb-5">
        <a href="#form" class="btn btn-lg btn-white">Зарегистрироваться</a>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'WhatToTalk',
    data: () => ({
      cards: [
        {
          image: require('@/assets/img/Group 24.svg'),
          description:
            'Каковы ситуации, при которых рекомендован управленческий аудит?'
        },
        {
          image: require('@/assets/img/Group 23.svg'),
          description:
            'Как управленческий аудит позволяет почти в режиме онлайн повышать эффективность бизнеса?'
        },
        {
          image: require('@/assets/img/Group 25.svg'),
          description:
            'Как управленческий аудит поможет масштабировать бизнес и наладить устойчивый рост?'
        }
      ]
    })
  }
</script>

<style scoped></style>
