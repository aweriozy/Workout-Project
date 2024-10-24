<template>
  <div class="videos">
    <!-- Первый блок -->
    <div class="video" @click="toggleVideo(0)">
      <p class="nomer">01</p>
      <div class="info">
        <h4>Упражнения дома</h4>
        <p>15 видео</p>
      </div>
      <div class="icon"><i class="fa-solid fa-arrow-right"></i></div>
      <div :class="['video__open', { open: videos[0] }]">
        <p><mark>Первый видео-урок БЕСПЛАТНЫЙ</mark></p>
        <iframe
          width="560"
          height="315"
          src="https://www.youtube.com/embed/IZaWksgybZM?si=63X0niIk1jkjOQgg"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <!-- Второй блок -->
    <div class="video" @click="toggleVideo(1)">
      <p class="nomer">02</p>
      <div class="info">
        <h4>Оставайся в форме</h4>
        <p>48 видео</p>
      </div>
      <div class="icon"><i class="fa-solid fa-arrow-right"></i></div>
      <div :class="['video__open', { open: videos[1] }]">
        <p><mark>Первый видео-урок БЕСПЛАТНЫЙ</mark></p>
        <iframe
          width="560"
          height="315"
          src="https://www.youtube.com/embed/fG-p3lgTOa8?si=-kwiEHheQmr6b9jF"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <!-- Третий блок -->
    <div class="video" @click="toggleVideo(2)">
      <p class="nomer">03</p>
      <div class="info">
        <h4>Интенсив</h4>
        <p>25 видео</p>
      </div>
      <div class="icon"><i class="fa-solid fa-arrow-right"></i></div>
      <div :class="['video__open', { open: videos[2] }]">
        <p><mark>Первый видео-урок БЕСПЛАТНЫЙ</mark></p>
        <iframe
          width="560"
          height="315"
          src="https://www.youtube.com/embed/Ib44QCcjsU8?si=uELSv7_ddOOEpexO"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <!-- Четвертый блок -->
    <div class="video" @click="toggleVideo(3)">
      <p class="nomer">04</p>
      <div class="info">
        <h4>Простые упражнения</h4>
        <p>35 видео</p>
      </div>
      <div class="icon"><i class="fa-solid fa-arrow-right"></i></div>
      <div :class="['video__open', { open: videos[3] }]">
        <p><mark>Первый видео-урок БЕСПЛАТНЫЙ</mark></p>
        <iframe
          width="560"
          height="315"
          src="https://www.youtube.com/embed/lMjnDtxxqjk?si=pEIFSVeN50Uzyb3U"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <!-- Пятый блок -->
    <div class="video" @click="toggleVideo(4)">
      <p class="nomer">05</p>
      <div class="info">
        <h4>Сжигание калорий</h4>
        <p>35 видео</p>
      </div>
      <div class="icon"><i class="fa-solid fa-arrow-right"></i></div>
      <div :class="['video__open', { open: videos[4] }]">
        <p><mark>Первый видео-урок БЕСПЛАТНЫЙ</mark></p>
        <iframe
          width="560"
          height="315"
          src="https://www.youtube.com/embed/RlaVIMbn2bY?si=Y55j8cvwTHc1wYnc"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin"
          allowfullscreen
        ></iframe>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      videos: [false, false, false, false, false],
    };
  },
  methods: {
    toggleVideo(index) {
      // Закрываем другие блоки и открываем выбранный
      this.videos = this.videos.map((video, i) =>
        i === index ? !video : false
      );
    },
  },
};
</script>

<style lang="scss" scoped>
.videos {
  margin-top: 250px;
}

.video {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 40px 0;
  cursor: pointer;
  transition: all 600ms ease;
  flex-wrap: wrap;
  flex-direction: column;

  &:not(:last-of-type) {
    border-bottom: 0.5px solid #666666;
  }

  &:hover {
    background-color: #1d1d1d;

    i {
      transform: rotate(90deg);
      transition: all 600ms ease;
    }
  }

  .nomer {
    color: #575757;
    font-weight: 600;
    font-size: 1.2em;
  }

  .info {
    @media (min-width: 630px) {
      width: 450px;
    }

    @media (max-width: 630px) {
      width: 200px;
    }

    h4 {
      font-weight: 400;

      @media (min-width: 630px) {
        font-size: 2.5em;
      }

      @media (max-width: 630px) {
        font-size: 1.5em;
      }
    }

    p {
      color: #6f6f6f;
      margin-top: 10px;
    }
  }

  i {
    margin-right: 20px;
  }

  .video__open {
    overflow: hidden;
    max-height: 0;
    transition: max-height 0.6s ease, padding 0.6s ease;
    padding: 0;
  }

  .video__open.open {
    max-height: 1000px; /* Настраиваемая высота для плавного открытия */
    padding: 20px 0;
  }

  .video__open p {
    margin-left: 130px;
    margin-bottom: 30px;
    font-weight: 600;
    font-size: 1.05em;

    mark {
      background-color: #25ab76;
      padding: 5px;
    }
  }
}
</style>
