<template>
  <div class="footer-links">
    <img
      v-for="link in socialLinks"
      :key="link.alt"
      :src="link.src"
      :alt="link.alt"
      class="footer-links__icon"
    />
  </div>
</template>

<script setup lang="ts">
const socialLinks = [
  { src: '/icons/vk.svg', alt: 'vk' },
  { src: '/icons/telegram.svg', alt: 'telegram' },
  { src: '/icons/JJ-icon.svg', alt: 'JJ' },
  { src: '/icons/JJ-icon.svg', alt: 'JJ' },
];
</script>

<style scoped lang="scss">
.footer-links {
  display: flex;
  gap: 1em;

  &__icon {
    background: white;
    border-radius: 50%;
    padding: 0.5em;
    cursor: pointer;
  }
}
</style>
