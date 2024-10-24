<template>
  <div>
    <div class="features">
      <div class="features__heading">
        <img src="/img/yellow-line.svg" alt="Workout" />
        <h3>Тренировки Специально Для Тебя</h3>
      </div>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates,
        accusantium ducimus magnam iure reiciendis eaque?
      </p>
      <button type="button">Начать</button>
    </div>
    <div class="pictures">
      <div>
        <img src="/img/trener-1.png" alt="trener" />
        <h4>Саманта Вильям</h4>
        <p>Тренер</p>
      </div>
      <div class="middle">
        <img src="/img/trener-2.png" alt="trener" />
        <h4>Алина Реймонд</h4>
        <p>Тренер</p>
      </div>
      <div class="big">
        <img src="/img/trener-3.png" alt="trener" />
        <h4>Джонатан Вайз</h4>
        <p>Тренер</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.features {
  width: 1500px;
  background-color: #191919;
  position: relative;
  padding: 120px 5% 270px 15%;

  @media (min-width: 1380px) {
    margin-left: 391px;
  }

  @media (max-width: 1380px) and (min-width: 1100px) {
    margin-left: 191px;
  }

  @media (min-width: 1100px) {
    padding: 120px 5% 270px 15%;
  }

  @media (max-width: 1100px) {
    padding: 50px;
  }

  p {
    color: #ababab;
    line-height: 170%;
    @media (min-width: 1100px) {
      margin-left: 200px;
    }

    @media (min-width: 1100px) {
      font-size: 1.3em;
      width: 500px;
    }

    @media (max-width: 560px) {
      font-size: 3.05em;
      width: 250px;
    }
  }

  button {
    @media (min-width: 1100px) {
      margin-left: 200px;
    }
    background-color: #25ab76;
    padding: 20px;
    width: 160px;
    font-weight: 600;
    font-size: 18px;
    color: #fff;
    border: 0;
    border-radius: 10px;
    margin-top: 30px;
    cursor: pointer;
    transition: all 600ms ease;

    &:hover {
      transform: translateY(7px);
    }
  }

  .features__heading {
    position: absolute;
    left: -230px;
    top: 40px;
    @media (min-width: 1100px) {
      position: absolute;
      top: 0px;
      left: -230px;
    }

    h3 {
      @media (min-width: 1100px) {
        position: relative;
        top: -100px;
      }

      @media (min-width: 560px) {
        font-size: 4.5em;
        width: 500px;
      }

      @media (max-width: 560px) {
        font-size: 2.3em;
        width: 300px;
      }
    }

    img {
      position: relative;
      top: 320px;
      @media (min-width: 1100px) {
        position: relative;
        top: 330px;
      }
    }
  }
}

.pictures {
  margin-bottom: 100px;
  display: flex;

  @media (min-width: 1380px) {
    padding-left: 70px;
  }

  @media (max-width: 1380px) and (min-width: 1100px) {
    position: relative;
    left: -127px;
  }

  @media (max-width: 1100px) {
    flex-wrap: wrap;
    justify-content: space-between;
  }
  > div {
    @media (min-width: 1100px) {
      position: relative;
    }

    @media (max-width: 1100px) {
      margin-top: 100px;
    }

    &.middle {
      top: 321px;
    }

    &.big {
      top: -193px;

      h4,
      p {
        margin-left: 20px;
      }
    }

    h4 {
      font-weight: 400;
    }
    p {
      color: #ababab;
      font-size: 0.9em;
    }
  }
}
</style>
