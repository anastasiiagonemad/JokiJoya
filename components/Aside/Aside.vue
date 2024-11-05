<template>
  <aside class="aside">
    <nav class="aside__nav">
      <AsideLink title="Парки" iconSrc="/icons/menu-arrow.svg" />
      <AsideLink title="Праздники" iconSrc="/icons/menu-arrow.svg" />
      <AsideLink title="Рестораны" iconSrc="/icons/menu-arrow.svg" />
      <AsideLink title="Афиша" />
    </nav>
  </aside>
</template>

<script setup lang="ts">
import AsideLink from './AsideLink.vue';
</script>

<style lang="scss" scoped>
@import '../../assets/styles/main.scss';

.aside {
  background-color: $aside-bg;
  display: flex;
  height: 100%;
  justify-content: center;

  &__nav {
    display: flex;
    flex-direction: column;
    gap: 100px;
    color: #ffffff;
    font-family: 'DrukCyrMed', sans-serif;
    text-transform: uppercase;
    font-size: 1.375em;
    line-height: 1.5em;
    align-items: center;
    margin-top: 8.75em;
  }
}

@media screen and (max-width: 768px) {
  .aside {
    display: none;
  }
}
</style>
