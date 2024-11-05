<script lang="ts">
import MainPic from './MainPic.vue';
import MainTitle from './MainTitle.vue';
import MainContainer from './MainContainer.vue';
</script>

<template>
  <div class="main">
    <MainPic />
    <MainTitle />
    <MainContainer />
  </div>
</template>

<style lang="scss">
.main {
  background: url('../../public/images/main-bg.jpeg');
}
</style>
