<template>
  <div class="head">
    <div class="promotion">
      <span>NEW</span>
      Новая интенсивная тренировка
    </div>
    <div class="lead">
      <div class="right">
        <h1>
          Cardio<br />
          Exercise
        </h1>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Velit,
          dolore aspernatur sequi soluta porro sit.
        </p>
        <div class="lead__buttons">
          <button>Начать</button>
          <button>Детальнее</button>
        </div>
      </div>
      <div class="left">
        <img src="/img/lead.png" alt="Workout" />
        <div class="lead_info">
          <div class="lead_info_time">
            <span>{{ showTime }}</span>
            ВРЕМЯ
          </div>
          <div class="lead_info_cl">
            <span>165</span>
            КАЛОРИИ
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showTime: "40:00",
      timerCount: 39 * 60,
    };
  },
  watch: {
    timerCount: {
      handler() {
        setTimeout(() => {
          if (this.timerCount <= 0) return;

          this.timerCount--;
          const minutes = Math.ceil(this.timerCount / 60);
          const seconds = this.timerCount - minutes * 60 + 60;
          let txtSeconds = 0;
          if (seconds == 60) txtSeconds = "00";
          else if (seconds < 10 && seconds > 0) txtSeconds = "0" + seconds;
          else txtSeconds = seconds;
          this.showTime =
            (txtSeconds == "00" ? minutes + 1 : minutes) + ":" + txtSeconds;
        }, 1000);
      },
      immediate: true,
    },
  },
};
</script>
<style lang="scss" scoped>
.head {
  margin-top: 70px;

  @media (min-width: 1024px) {
    overflow: hidden;

    width: auto;
  }
}

@keyframes pulse {
  0% {
    transform: scale(0.95);
  }
  100% {
    transform: scale(1.1);
  }
}

.promotion {
  background-color: #191919;
  border-radius: 200px;
  padding: 10px 5px;
  color: #d1d1d1;
  margin-left: 20px;
  width: 350px;
  animation: pulse infinite ease-in-out 1.5s alternate;

  @media (min-width: 450px) {
    width: 350px;
  }

  @media (max-width: 450px) {
    width: 270px;
    font-size: 0.85em;
    margin-left: 5px;
    @keyframes pulse {
      0% {
        transform: scale(0.8);
      }
      100% {
        transform: scale(1);
      }
    }
  }
  span {
    background-color: #25ab75;
    border-radius: 200px;
    padding: 5px 10px;
    color: #fff;
    margin-right: 10px;
    font-weight: 600;
  }
}

.lead {
  margin-top: 20px;
  display: flex;
  position: relative;

  .left {
    margin-left: -247px;
    height: 720px;
  }

  h1 {
    letter-spacing: -2px;

    @media (min-width: 1500px) {
      font-size: 12em;
      line-height: 170px;
    }

    @media (max-width: 1500px) and (min-width: 1300px) {
      font-size: 11em;
      line-height: 160px;
    }

    @media (max-width: 1300px) and (min-width: 650px) {
      font-size: 8.5em;
      line-height: 150px;
    }

    @media (max-width: 650px) and (min-width: 450px) {
      font-size: 5.5em;
      line-height: 110px;
    }

    @media (max-width: 450px) {
      font-size: 4em;
      line-height: 90px;
    }
  }
  p {
    color: #868686;
    margin-top: 20px;
    margin-bottom: 20px;

    @media (min-width: 650px) {
      width: 600px;
    }
  }

  .lead__buttons > button {
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

    @media (min-width: 320px) and (max-width: 1024px) {
      width: 280px;
    }

    &:first-of-type {
      margin-right: 35px;
    }

    &:last-of-type {
      background-color: #191919;
      //   margin-left: 35px;
    }

    &:hover {
      transform: translateY(7px);
    }
  }
  > div:last-of-type {
    @media (max-width: 1024px) {
      display: none;
    }
    img {
      position: relative;

      @media (min-width: 1480px) {
        bottom: 255px;
        right: 60px;
      }

      @media (max-width: 1470px) and (min-width: 1300px) {
        transform: scale(0.7);
        bottom: 400px;
        right: 100px;
      }

      @media (max-width: 1300px) {
        transform: scale(0.7);
        bottom: 400px;
        right: 100px;
      }
    }

    .lead_info {
      position: absolute;
      top: 0;
      right: 0;

      @mixin info-block {
        background-color: #191919;
        border-radius: 20px;
        padding: 20px 30px;
        width: 110px;
        font-size: 0.7em;
        margin-bottom: 25px;

        span {
          font-weight: 600;
          font-size: 3em;
          display: block;
        }
      }

      .lead_info_time {
        @include info-block;

        span {
          color: #ffe642;
        }
      }

      .lead_info_cl {
        @include info-block;

        span {
          color: #fb1351;
        }
      }
    }
  }
}
</style>
