<template>
  <div class="footer-about">
    <div class="footer-about__site">
      <p>Joki Joya ©</p>
      <p>2023</p>
      <a href="https://joki-joya.ru" target="_blank">joki-joya.ru</a>
    </div>
    <button class="footer-about__button" @click="$emit('scrollToTop')">
      Наверх <img src="/icons/icon5.svg" alt="arrow up" />
    </button>
  </div>
</template>

<style scoped lang="scss">
.footer-about {
  display: flex;
  align-items: center;
  text-align: center;
  color: white;
  gap: 3em;

  @media screen and (max-width: 375px) {
    flex-direction: column;
  }

  &__site {
    font-family: 'NunitoBlack', sans-serif;
    font-size: 0.875em;

    a {
      color: white;
      text-decoration: none;
    }
  }

  &__button {
    display: flex;
    align-items: center;
    padding: 0.5em 2em;
    border: 2px solid white;
    color: white;
    background: none;
    border-radius: 50px;
    text-transform: uppercase;
    cursor: pointer;
    font-family: 'DrukCyrMed', sans-serif;
    font-size: 1.375em;
    gap: 0.5em;
  }
}
</style>
