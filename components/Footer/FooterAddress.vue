<template>
  <div class="footer-address">
    <div class="footer-address__logo">
      <p>Joki</p>
      <div class="footer-address__icons">
        <img v-for="icon in icons" :key="icon" :src="icon" alt="icon" />
      </div>
      <p>Joya</p>
    </div>
    <div class="footer-address__phone">
      <p><span>+7 (495) 181 22 77</span></p>
      <p>(МОСКВА, ТВЕРЬ)</p>
      <p><span>+7 (812) 635 22 77</span></p>
      <p>(САНКТ-ПЕТЕРБУРГ)</p>
    </div>
  </div>
</template>

<script setup lang="ts">
const icons = [
  '/icons/icon4.svg',
  '/icons/icon1.svg',
  '/icons/icon2.svg',
  '/icons/icon3.svg',
];
</script>

<style scoped lang="scss">
@import '../../assets/styles/main.scss';
.footer-address {
  display: flex;
  gap: 3em;
  align-items: center;
  color: white;
  text-transform: uppercase;
  font-family: 'DrukCyrWide', sans-serif;

  @media screen and (max-width: 375px) {
    flex-direction: column;
    text-align: center;
  }

  &__logo {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5em;

    p {
      font-size: 1.375em;
    }

    &__icons {
      display: flex;
      gap: 0.125em;
    }
  }

  &__phone {
    display: flex;
    flex-direction: column;
  }

  &__phone span {
    color: $btn-lightGreen;
  }
}
</style>
