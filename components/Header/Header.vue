<template>
  <header class="header">
    <div class="header__leftSide">
      <div class="header__leftSide-logo">
        <img src="../../public/icons/JJ.svg" alt="logoJJ" />
      </div>
      <div class="header__leftSide-btns">
        <div class="header__leftSide-btns-map">
          <img src="../../public/icons/map.svg" alt="iconMap" />
          <p>Москва</p>
        </div>
        <div class="header__leftSide-btns-phone">
          <img src="../../public/icons/phone.svg" alt="iconPhone" />
          <p>+7 (812) 635 22 77</p>
        </div>
      </div>
    </div>

    <div class="header__rightSide">
      <div class="header__rightSide-btns">
        <div class="header__rightSide-btns-buy">
          <button>Купить билеты</button>
        </div>
        <div class="header__rightSide-btns-reserve">
          <button>Заказать праздник</button>
        </div>
      </div>
      <div class="header__rightSide-menu">
        <div class="header__rightSide-menu-span">
          <span class="header__rightSide-menu-span-top"></span>
          <span class="header__rightSide-menu-span-middle"></span>
          <span class="header__rightSide-menu-span-end"></span>
        </div>
        <div class="header__rightSide-menu-title">
          <p>Меню</p>
        </div>
      </div>
    </div>
    <div class="header__bottom"></div>
  </header>
</template>

<script lang="ts"></script>

<style lang="scss">
@import '../../assets/styles/main.scss';

.header {
  background: transparent;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.75em 1em;
  width: 100%;
  max-width: 1440px;
  margin: 0 auto;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  font-family: 'DrukCyrMed', sans-serif;
  z-index: 100000;

  &::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: $header-bg;
    filter: blur(3px);
    z-index: -1;
  }

  &__leftSide {
    display: flex;
    align-items: center;
    gap: 3.5em;
    color: $border;
    flex: 1;

    &-logo {
      display: flex;
      cursor: pointer;
    }
    &-btns {
      display: flex;
      gap: 1em;

      &-map {
        display: flex;
        align-items: center;
        text-transform: uppercase;
        gap: 3px;
        padding: 0.5em 1em;
        border: 2px solid $border;
        border-radius: 30px;
        font-size: 1.375em;
        line-height: 1.5em;
        text-align: center;
        cursor: pointer;
        letter-spacing: 1px;
      }
      &-phone {
        display: flex;
        align-items: center;
        font-family: 'DrukCyrWide', sans-serif;
        gap: 3.5px;
        padding: 0.687em 1em;
        border: 2px solid $border;
        border-radius: 30px;
        cursor: pointer;
      }
    }
  }

  &__rightSide {
    display: flex;
    align-items: center;
    gap: 3.5em;
    flex: 1;

    &-btns {
      display: flex;
      gap: 1em;

      &-buy {
        display: flex;
        button {
          font-family: 'DrukCyrMed', sans-serif;
          text-transform: uppercase;
          line-height: 1.5em;
          font-size: 1.375em;
          letter-spacing: 1px;
          background: $btn-pink;
          border: none;
          color: #ffffff;
          border-radius: 30px;
          padding: 0.437em 2em 0.562em 2em;
          cursor: pointer;
        }
      }
      &-reserve {
        display: flex;
        button {
          font-family: 'DrukCyrMed', sans-serif;
          text-transform: uppercase;
          line-height: 1.5em;
          font-size: 1.375em;
          letter-spacing: 1px;
          background: $btn-lightGreen;
          border: none;
          color: #000000;
          border-radius: 30px;
          padding: 0.437em 2em 0.562em 2em;
          cursor: pointer;
        }
      }
    }
    &-menu {
      cursor: pointer;
      &-span {
        display: flex;
        flex-direction: column;
        gap: 6px;
        transform: rotate(180deg);

        &-top {
          background-color: $menuSpan;
          width: 2em;
          height: 4px;
        }
        &-middle {
          background: $menuSpan;
          width: 1.375em;
          height: 4px;
        }
        &-end {
          background: $menuSpan;
          width: 2em;
          height: 4px;
        }
      }

      &-title {
        text-transform: uppercase;
        color: $menuSpan;
        font-family: 'Montserrat', sans-serif;
        padding-top: 0.375em;
      }
    }
  }
}

@media screen and (max-width: 768px) {
  .header {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    padding: 0.75em 1em;

    &__leftSide {
      flex: 1;
      justify-content: space-around;
      &-btns {
        display: none;
      }
      &-logo {
        margin-right: auto;
      }
    }

    &__rightSide {
      display: flex;
      align-items: center;
      justify-content: space-around;
      gap: 3.5em;
      flex: 1;

      &-btns {
        text-wrap: nowrap;
        margin-left: -100px;
        display: block;
        justify-content: space-around;
        &-reserve {
          display: none;
        }
      }
    }
  }
}
</style>
