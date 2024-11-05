<template>
  <div class="main__title">
    <div class="main__title-text">
      <div class="main__title-text-about">
        <p>О</p>
      </div>

      <div class="main__title-text-brand">
        <div class="main__title-text-brand-layout">
          <p>JOKI JOYA</p>
        </div>
        <div class="main__title-text-brand-center">
          <p>JOKI JOYA</p>
        </div>
      </div>

      <div class="main__title-text-pic">
        <img
          class="main__title-text-pic-1"
          src="../../public/icons/blue-star.svg"
          alt="blue star icon"
        />
        <img
          class="main__title-text-pic-2"
          src="../../public/icons/blue-star.svg"
          alt="blue star icon"
        />
        <img
          class="main__title-text-pic-3"
          src="../../public/icons/blue-star.svg"
          alt="blue star icon"
        />
      </div>
    </div>

    <div class="main__title-logo">
      <img src="../../public/images/welvome.svg" alt="JJ logo" />
    </div>
  </div>
</template>

<style lang="scss">
@import '../../assets/styles/main.scss';
.main__title {
  display: flex;
  justify-content: center;
  gap: 15%;
  font-size: 4.5em;
  font-family: 'DrukCyrWide';

  &-text {
    display: flex;
    align-items: center;
    margin-top: -50px;

    &-about {
      margin-right: 5px;
    }

    &-brand {
      position: relative;
      margin-right: 20px;
      &-center {
        position: relative;
        color: $menuSpan;
      }
      &-layout {
        position: absolute;
        top: 5px;
        right: -10px;
        p {
          color: transparent;
          -webkit-text-stroke: 3px $btn-lightGreen;
          background-clip: text;
        }
      }
    }

    &-pic {
      display: flex;
      gap: 19px;
    }
  }

  &-logo {
    margin-top: 50px;
  }
}

@media screen and (max-width: 375px) {
  .main__title {
    margin: 1em 0 0 0.5em;
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 0;
    font-size: 3.5em;
    font-family: 'DrukCyrWide';

    &-text {
      &-about,
      &-brand {
        p {
          font-size: 0.5em;
        }
      }
      &-pic {
        &-2,
        &-3 {
          display: none;
        }
      }
    }

    &-logo {
      margin-top: 50px;
    }
  }
}
</style>
