<template>
  <div class="head">
    <div class="lead">
      <div class="right">
        <h1>
          Cardio<br />
          Exercise
        </h1>
        <p>
          Огромный выбор материалов о здоровье и фитнесе, полезных<br />
          рецептов и историй преображения, которые помогут вам <br />
          привести себя в форму и оставаться в форме!
        </p>
        <button>Присоединяйтесь</button>
        <img src="/img/companies.png" alt="companies" />
      </div>
      <div class="left">
        <img src="/img/lead2.png" alt="Workout" />
        <div class="lead_info">
          <div class="lead_info_km">
            <i
              class="fa-sharp-duotone fa-solid fa-person-running fa-beat-fade"
            ></i>
            <span>4.95</span>
            km
          </div>
          <div class="lead_info_training">
            <i class="fa-solid fa-circle-play fa-shake"></i>
            <span>350+</span>
            Тренировок
          </div>
          <div class="lead_info_videos">
            <span>500+</span>
            Бесплатных видео
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.head {
  margin-top: 70px;

  @media (min-width: 1024px) {
    overflow: hidden;

    width: auto;
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

  button {
    background-color: #e6533c;
    padding: 20px;
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

    &:hover {
      transform: translateY(7px);
    }
  }

  > div:first-of-type img {
    display: block;
    max-width: 100%;
    margin-top: 70px;
  }
  > div:last-of-type {
    @media (max-width: 1024px) {
      display: none;
    }
    img {
      position: relative;

      @media (min-width: 1480px) {
        top: 20px;
        right: -180px;
      }

      @media (max-width: 1470px) and (min-width: 1300px) {
        transform: scale(0.85);
        top: 10px;
        right: -150px;
      }

      @media (max-width: 1300px) {
        transform: scale(0.7);
        bottom: 30px;
        right: -90px;
      }
    }

    .lead_info {
      position: absolute;
      top: 0;
      right: 0;

      @mixin info-block {
        border-radius: 20px;
        padding: 20px 30px;
        width: 110px;
        font-size: 0.7em;
        margin-bottom: 25px;
        position: relative;

        span {
          font-weight: 600;
          color: #fff;
        }

        i {
          padding: 10px;
          border-radius: 50%;
          color: #fff;
          font-size: 1.3em;
          text-align: center;
          width: 14px;
          height: 14px;
          line-height: 14px;
        }
      }

      .lead_info_km {
        @include info-block;
        background-color: #ef8964;
        color: #efcaba;
        right: 20px;
        top: 5px;

        span {
          font-size: 2.7em;
          margin-top: 4px;
        }

        i {
          display: block;
          background-color: #efa082;
          font-size: 1.8em;
        }
      }

      .lead_info_training {
        @include info-block;
        background-color: #303030;
        color: #acaba8;
        top: 250px;
        @media (min-width: 1450px) {
          right: 400px;
        }

        @media (max-width: 1450px) and (min-width: 1100px) {
          right: 270px;
        }

        @media (max-width: 1100px) {
          right: 180px;
        }

        span {
          font-size: 1.7em;
        }

        i {
          width: 14px;
          height: 14px;
          margin-right: 7px;
          background-color: #ef8963;
          font-size: 1.8em;
          padding-left: 10px;
          float: left;
          position: relative;
          top: 5px;
          text-align: center;
        }
        .fa-circle-play {
          padding-right: 15px;
          padding-top: 15px;
        }
      }

      .lead_info_videos {
        @include info-block;
        background-color: #7a29dc;
        color: #c6a8e4;
        right: 0;
        top: 250px;

        span {
          font-size: 2.5em;
        }
      }
    }
  }
}
</style>
