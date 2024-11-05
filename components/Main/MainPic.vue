<template>
  <div class="main__pic">
    <img src="../../public/images/pic1.jpg" alt="" />
  </div>
</template>

<style lang="scss">
.main__pic {
  display: flex;
  justify-content: center;
  margin-top: -25px;
  @media screen and (max-width: 375px) {
    margin-top: 0px;
    img {
      height: 450px;
    }
  }
  img {
    width: 90%;
  }
}
</style>
