<template>
  <div class="aside-link">
    <p>{{ title }}</p>
    <img v-if="iconSrc" :src="iconSrc" alt="arrow" />
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps<{
  title: string;
  iconSrc?: string;
}>();
</script>

<style lang="scss" scoped>
.aside-link {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.8125em;
  transform: rotate(-90deg);
  cursor: pointer;
  text-align: center;

  img {
    transform: rotate(90deg);
  }
}
</style>
