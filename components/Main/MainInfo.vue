<template>
  <div class="main__info">
    <div class="main__info-parks">
      <div class="main__info-parks-title">
        <p>Наши парки:</p>
        <img src="../../public/icons/rhombus.png" alt="pic" />
      </div>

      <div class="main__info-parks-inform">
        <h4>Первый парк развлечений Joki Joya</h4>
        <p>
          открылся в августе 2014 года в Санкт-Петербурге. Сегодня бренд Joki
          Joya является лидером индустрии детских развлечений в России и состоит
          из 28 парков в 3 городах: 17 в Москве и Московской области, 10 в
          Санкт-Петербурге и 1 в Твери. На территории каждого парка размещено
          более 30 аттракционов в игровой зоне, семейный ресторан с детским и
          взрослым меню, индивидуальные банкетные комнаты для проведения
          праздников.
        </p>
      </div>

      <div class="main__info-parks-address">
        <p>
          Площадь парков от 2000 до 6000 квадратных метров в зависимости от ТРЦ.
        </p>
        <p>
          Также Joki Joya занимается организацией праздников «под ключ»: детские
          дни рождения, выпускные детского сада или школы, Новый Год,
          корпоративные праздники.
        </p>
        <button>
          <p>Посмотреть адреса</p>
          <img src="../../public/icons/arrow-black.svg" alt="arrow" />
        </button>
      </div>
    </div>

    <div class="main__info-celebrate">
      <div class="main__info-celebrate-title">
        <p>Праздники у нас:</p>
        <img src="../../public/icons/flower.png" alt="pic" />
      </div>

      <div class="main__info-celebrate-inform">
        <p>
          Праздник можно отметить в индивидуальной банкетной комнате,
          расписанной профессиональными художниками вручную под тематику
          популярных фильмов или мультфильмов, либо в семейном ресторане.
        </p>
        <br />
        <p>
          Что мы имеем в виду, когда говорим про организацию праздников «под
          ключ»? За каждым праздником мы закрепляем личного банкетного
          менеджера, который будет курировать ваш праздник.
        </p>
      </div>

      <div class="main__info-celebrate-address">
        <p>
          В нашей базе более 300 аниматоров, шоу-программ и квестов, которые
          помогут создать особую атмосферу праздника. Украсят ваш праздник
          профессиональные аквагримеры, лучшие торты на заказ, а также фото — и
          видеосъемка.
        </p>
        <br />
        <p>
          <span>Joki Joya</span> - это целая история про детей и их родителей.
          История, которая помогает семьям объединяться, окунаться с головой в
          детство и проводить время вместе, забывая о повседневной суёте.
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.main__info {
  grid-area: Container;
  display: flex;
  flex-direction: column;
  gap: 8.125em;
  &-parks,
  &-celebrate {
    display: grid;
    grid-template-columns: auto auto auto;
    gap: 7.0625em;
    &-title {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
      width: 10em;
      font-family: 'DrukCyrWide', sans-serif;
      text-transform: uppercase;

      img {
        align-self: flex-start;
      }
    }
    &-inform {
      width: 20.625em;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      font-family: 'NunitoLight', sans-serif;
      line-height: 1.5em;
      font-size: 1em;
      h4 {
        font-family: 'NunitoBlack', sans-serif;
      }
    }

    &-address {
      width: 20.625em;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      font-family: 'NunitoLight', sans-serif;
      line-height: 1.5em;
      span {
        font-family: 'NunitoBlack', sans-serif;
      }
      button {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0.687em 1.328em 0.8125em 1.093em;
        width: 13.437em;
        border: 2px solid black;
        border-radius: 48px;
        cursor: pointer;
        background: none;

        p {
          font-family: 'DrukCyrMed', sans-serif;
          text-transform: uppercase;
          letter-spacing: 1px;
          font-size: 1.375em;
        }
      }
    }
  }
}

@media screen and (max-width: 375px) {
  .main__info {
    grid-area: Container;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;

    &-parks,
    &-celebrate {
      display: grid;
      grid-template-columns: 1fr;

      gap: 1em;
      &-title {
        display: flex;
        flex-direction: row-reverse;
        justify-content: start;
        gap: 2em;
        align-items: center;
        width: 80%;
        font-family: 'DrukCyrWide', sans-serif;
        text-transform: uppercase;

        img {
          width: 50px;
        }
      }
      &-inform {
        width: 80%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        font-family: 'NunitoLight', sans-serif;
        line-height: 1.5em;
        font-size: 1em;
        h4 {
          font-family: 'NunitoBlack', sans-serif;
        }
      }

      &-address {
        width: 80%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        font-family: 'NunitoLight', sans-serif;
        line-height: 1.5em;
        span {
          font-family: 'NunitoBlack', sans-serif;
        }
        button {
          display: none;
        }
      }
    }
  }
}
</style>
