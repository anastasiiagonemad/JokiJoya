<template>
  <div class="main__line">
    <div class="main__line-show">
      <p>JJ SHOW</p>
      <img src="../../public/icons/✽.svg" alt="" />
    </div>

    <div class="main__line-celebrate">
      <p>Celebrate</p>
      <img src="../../public/icons/✽.svg" alt="" />
    </div>

    <div class="main__line-birthday">
      <p>birthday</p>
      <img src="../../public/icons/✽.svg" alt="" />
    </div>

    <div class="main__line-show">
      <p>JJ SHOW</p>
      <img src="../../public/icons/✽.svg" alt="" />
    </div>

    <div class="main__line-quests">
      <p>quests</p>
      <img src="../../public/icons/✽.svg" alt="" />
    </div>
  </div>
</template>

<style lang="scss">
.main__line {
  grid-area: Line;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  gap: 250px;
  margin-top: 170px;
  margin-left: 100px;
  &-show,
  &-celebrate,
  &-birthday,
  &-quests {
    display: flex;
    align-items: center;
    gap: 40px;
    transform: rotate(-90deg);
    transform-origin: left center;
    p {
      font-size: 5.25em;
      text-wrap: nowrap;
      color: transparent;
      -webkit-text-stroke: 1.2px black;
      text-transform: uppercase;
      font-family: 'DrukCyrMed', sans-serif;
    }
  }
}

@media screen and (max-width: 375px) {
  .main__line {
    grid-area: Line;
    margin-top: 0em;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    gap: 5em;
    margin-left: 3em;
    &-show,
    &-celebrate,
    &-birthday,
    &-quests {
      display: flex;
      align-items: center;
      gap: 40px;
      transform: rotate(-90deg);
      transform-origin: left center;
      p {
        font-size: 3em;
        text-wrap: nowrap;
        color: transparent;
        -webkit-text-stroke: 1.2px black;
        text-transform: uppercase;
        font-family: 'DrukCyrMed', sans-serif;
      }
      img {
        width: 50px;
      }
    }
  }
}
</style>
