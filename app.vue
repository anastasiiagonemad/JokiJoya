<script setup lang="ts">
import Header from './components/Header/Header.vue';
import Aside from './components/Aside/Aside.vue';
import Main from './components/Main/Main.vue';
import Slider from './components/Slider/Slider.vue';
import Footer from './components/Footer/Footer.vue';
</script>

<template>
  <div class="container">
    <Header />
    <Aside />
    <Main />
    <Slider />
    <Footer />
  </div>
</template>

<style lang="scss">
@import './assets/styles/main.scss';
</style>
