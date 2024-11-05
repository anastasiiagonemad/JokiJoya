<script lang="ts">
import MainLine from './MainLine.vue';
import MainInfo from './MainInfo.vue';
import MainInteractive from './MainInteractive.vue';
</script>

<template>
  <div class="main__container">
    <MainLine />
    <MainInfo />
    <MainInteractive />
  </div>
</template>
<style lang="scss">
.main__container {
  margin-top: 4.375em;
  display: grid;
  grid-template-areas:
    'Line Container'
    'Line Interactive';
  grid-template-columns: 13em auto;
}
@media screen and (max-width: 375px) {
  .main__container {
    margin-top: 4.375em;
    display: grid;
    grid-template-areas:
      'Line Container .'
      'Interactive Interactive .';
    grid-template-columns: 7em auto;
  }
}
</style>
