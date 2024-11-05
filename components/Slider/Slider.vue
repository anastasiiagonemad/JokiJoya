<template>
  <div class="slider">
    <div class="slider__title">
      <div class="slider__title-interiors">
        <p>Интерьеры</p>
        <img src="../../public/icons/blue-star.svg" alt="blue star" />
        <img src="../../public/icons/blue-star.svg" alt="blue star" />
      </div>

      <div class="slider__title-parks">
        <div class="slider__title-parks-icons">
          <img src="../../public/icons/cross-thin-gradient.svg" alt="icon" />
          <img src="../../public/icons/sun-gradient.svg" alt="" />
          <img src="../../public/icons/cross-gradient.svg" alt="icon" />
        </div>
        <div class="slider__title-parks-text">
          <p>Парков</p>
        </div>
      </div>
    </div>

    <div class="slider__carousel">
      <div class="slider__carousel-slides" :style="slideStyle">
        <div
          v-for="(image, index) in images"
          :key="index"
          :class="[
            'slider__carousel-slide',
            { active: index === currentIndex },
          ]"
        >
          <img :src="image" alt="slide pic" />
        </div>
      </div>

      <div class="slider__carousel-pagination">
        <span
          v-for="(image, index) in images"
          :key="index"
          :class="['dot', { active: index === currentIndex }]"
          @click="goToSlide(index)"
        ></span>
      </div>

      <div class="slider__carousel-btns">
        <button @click="prevSlide" class="slider__carousel-btns-prev">
          <img src="../../public/icons/arrow-black.svg" alt="prev" />
        </button>

        <button @click="nextSlide" class="slider__carousel-btns-next">
          <img src="../../public/icons/arrow-black.svg" alt="next" />
        </button>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { ref, defineComponent, computed } from 'vue';

export default defineComponent({
  name: 'Carousel',

  setup() {
    const currentIndex = ref(0);
    const images = [
      '/images/pic2.jpg',
      '/images/pic2.jpg',
      '/images/pic2.jpg',
      '/images/pic2.jpg',
      '/images/pic2.jpg',
      '/images/pic2.jpg',
    ];

    const goToSlide = (index: number) => {
      currentIndex.value = index;
    };

    const nextSlide = () => {
      currentIndex.value = (currentIndex.value + 1) % images.length;
    };

    const prevSlide = () => {
      currentIndex.value =
        (currentIndex.value - 1 + images.length) % images.length;
    };

    const slideStyle = computed(() => {
      return {
        transition: 'transform 0.5s ease',
        transform: `translateX(-${currentIndex.value * 100}%)`,
      };
    });

    return {
      currentIndex,
      goToSlide,
      nextSlide,
      prevSlide,
      images,
      slideStyle,
    };
  },
});
</script>

<style lang="scss">
@import '../../assets/styles/main.scss';

.slider {
  display: grid;
  grid-template-columns: 250px auto;

  &__title {
    margin-top: 300px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    transform: rotate(-90deg);

    &-interiors {
      display: flex;
      align-items: center;
      gap: 16px;
      p {
        font-family: 'DrukCyrMed', sans-serif;
        font-size: 75px;
        text-transform: uppercase;
      }
    }

    &-parks {
      position: relative;

      &-icons {
        display: flex;
        justify-content: space-around;
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        z-index: 100;
        margin-right: -100px;
      }

      &-text {
        position: relative;

        p {
          font-family: 'DrukCyrWide', sans-serif;
          text-transform: uppercase;
          font-size: 73px;
        }
      }
    }
  }

  &__carousel {
    overflow: hidden;
    position: relative;

    &-slides {
      padding: 0 0 0 80px;
      display: flex;
      transition: transform 0.5s ease;
      z-index: 1;

      &-slide {
        min-width: 100%;
        flex: 1;
        img {
          height: auto;
          width: 100%;
          position: relative;
        }
      }
    }

    &-btns {
      position: absolute;
      z-index: 50;
      display: flex;
      align-items: center;
      bottom: 50px;

      &-prev {
        background: $menuSpan;
        padding: 28.59px 22.87px;
        border: none;

        img {
          filter: invert(100%);
          transform: rotate(180deg);
        }
      }

      &-next {
        background: $btn-lightGreen;
        padding: 28.59px 22.87px;
        border: none;
      }
    }

    &-pagination {
      position: absolute;
      z-index: 200;
      bottom: 50px;
      left: 250px;
      display: flex;
      align-items: center;
      gap: 32px;

      .dot {
        cursor: pointer;
        width: 12px;
        height: 12px;
        border-radius: 50%;
        background-color: $btn-lightGreen;
      }
      .active {
        width: 64px;
        height: 16px;
        border-radius: 16px;
      }
    }
  }
}

@media screen and (max-width: 375px) {
  .slider {
    display: grid;
    grid-template-columns: 1fr;

    &__title {
      margin-top: 50px;
      margin-left: 10px;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: center;
      transform: rotate(0deg);

      &-interiors {
        display: flex;
        align-items: center;
        gap: 16px;
        p {
          font-family: 'DrukCyrMed', sans-serif;
          font-size: 50px;
          text-transform: uppercase;
        }
      }

      &-parks {
        position: relative;

        &-icons {
          display: none;
        }

        &-text {
          position: relative;

          p {
            font-family: 'DrukCyrWide', sans-serif;
            text-transform: uppercase;
            font-size: 60px;
          }
        }
      }
    }

    &__carousel {
      overflow: hidden;
      position: relative;

      &-slides {
        padding: 0;
        display: flex;
        transition: transform 0.5s ease;
        z-index: 1;

        &-slide {
          min-width: 100%;
          flex: 1;
          img {
            height: auto;
            width: 100%;
            position: relative;
          }
        }
      }

      &-btns {
        position: absolute;
        z-index: 50;
        display: flex;
        align-items: center;
        bottom: 0;
        top: -650px;
        left: 50px;

        &-prev {
          background: $menuSpan;
          padding: 28.59px 22.87px;
          border: none;

          img {
            filter: invert(100%);
            transform: rotate(180deg);
          }
        }

        &-next {
          background: $btn-lightGreen;
          padding: 28.59px 22.87px;
          border: none;
        }
      }

      &-pagination {
        position: absolute;
        z-index: 200;
        bottom: 50px;
        left: 50px;
        display: flex;
        align-items: center;
        gap: 32px;

        .dot {
          cursor: pointer;
          width: 12px;
          height: 12px;
          border-radius: 50%;
          background-color: $btn-lightGreen;
        }
        .active {
          width: 64px;
          height: 16px;
          border-radius: 16px;
        }
      }
    }
  }
}
</style>
