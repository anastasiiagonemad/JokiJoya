<template>
  <footer class="footer">
    <div class="footer__container">
      <FooterAddress />
      <FooterLinks />
      <FooterAbout @scrollToTop="scrollToTop" />
    </div>
  </footer>
</template>

<script setup lang="ts">
import FooterAddress from './FooterAddress.vue';
import FooterLinks from './FooterLinks.vue';
import FooterAbout from './FooterAbout.vue';

function scrollToTop() {
  window.scrollTo({ top: 0, behavior: 'smooth' });
}
</script>

<style lang="scss">
@import '../../assets/styles/main.scss';

.footer {
  background: $footer-bg;
  padding: 3em 7em;
  display: flex;
  justify-content: center;

  &__container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    gap: 2em;

    @media screen and (max-width: 375px) {
      display: flex;
      flex-direction: column;
      padding: 2em 1em;
      gap: 2em;
    }
  }
}
</style>
