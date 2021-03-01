<template>
  <div class="menu d-flex justify-content-end">
    <div
      class="menu-button"
      @click="isMenuOpen = !isMenuOpen"
      :class="{open: isMenuOpen}"
    >
      <div class="stick">
        <img src="@/assets/img/menu-button-stick.svg" alt="" />
      </div>
      <div class="stick">
        <img src="@/assets/img/menu-button-stick.svg" alt="" />
      </div>
      <div class="stick">
        <img src="@/assets/img/menu-button-stick.svg" alt="" />
      </div>
    </div>
    <nav
      class="nav my-4 animate__animated animate__delay-0.5s animate__fadeInDown animate__faster"
      :class="{'open-menu': isMenuOpen, 'close-menu': !isMenuOpen}"
    >
      <a href="#program" class="nav-link">Программа</a>
      <a href="#speaker" class="nav-link">Спикер</a>
      <a href="#form" class="nav-link">Регистрация</a>
    </nav>
  </div>
</template>

<script>
  export default {
    name: 'Menu',
    data: () => ({
      isMenuOpen: false
    })
  }
</script>

<style scoped></style>
