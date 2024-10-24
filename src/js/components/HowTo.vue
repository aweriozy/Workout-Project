<template>
  <div class="main">
    <h2>Не знаете с чего начать?</h2>
    <p>
      Программы предлагают ежедневные рекомендации в интерактивном календаре
    </p>
    <div class="blocks" :style="'left: ' + left + 'px'">
      <div class="item">
        <h3>Видео тренировки</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
        <i class="fa-solid fa-arrow-right"></i>
      </div>
      <div class="item">
        <h3>Программа курса</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
        <i class="fa-solid fa-arrow-right"></i>
      </div>
      <div class="item">
        <h3>Тарифы</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
        <i class="fa-solid fa-arrow-right"></i>
      </div>
      <div class="item">
        <h3>Полный доступ</h3>
        <p>Lorem ipsum dolor sit amet, consectetur, adipisicing elit.</p>
        <i class="fa-solid fa-arrow-right"></i>
      </div>
      <div class="item">
        <h3>Видео тренировок</h3>
        <p>Lorem ipsum dolor sit amet, consectetur, adipisicing elit.</p>
        <i class="fa-solid fa-arrow-right"></i>
      </div>
      <div class="item">
        <h3>Тарифы</h3>
        <p>Lorem ipsum dolor sit amet, consectetur, adipisicing elit.</p>
        <i class="fa-solid fa-arrow-right"></i>
      </div>
      <div class="item">
        <h3>Программа курса</h3>
        <p>Lorem ipsum dolor sit amet, consectetur, adipisicing elit.</p>
        <i class="fa-solid fa-arrow-right"></i>
      </div>
    </div>
    <div class="arrows">
      <img
        src="/img/arrow-next.svg"
        v-if="this.left != 0"
        @click="moveBlock('prev')"
        alt=""
      />
      <img
        src="/img/arrow-next.svg"
        @click="moveBlock('next')"
        v-if="this.left >= -1600"
        class="next"
        alt=""
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      left: 0,
    };
  },
  methods: {
    moveBlock(value) {
      let add = 320;

      if (value == "next" && this.left >= -1600) this.left -= add;
      else if (value == "prev" && this.left != 0) this.left += add;
    },
  },
};
</script>

<style lang="scss" scoped>
.main {
  overflow: hidden;
}

h2 {
  margin-top: 80px;
  font-size: 2.4em;
}

p {
  color: #9b9a97;
  margin-top: 15px;
}

.blocks {
  display: flex;
  margin-top: 35px;
  margin-bottom: 50px;
  width: 2500px;
  position: relative;
  left: -350px;
  transition: left 600ms ease;
}

.item {
  background-color: #323443;
  padding: 30px 25px;
  border-radius: 12px;
  width: 250px;
  transition: all 600ms ease;

  &:hover {
    cursor: pointer;
    opacity: 0.8;
  }

  p {
    color: #9b9a97;
  }

  &:not(:last-of-type) {
    margin-right: 25px;
  }

  i {
    float: right;
    font-size: 1.2em;
    position: relative;
    bottom: 25px;
  }
}

.arrows {
  img {
    cursor: pointer;
    transition: all 600ms ease;
    margin-right: 30px;
    margin-left: 10px;

    &:hover {
      transform: scale(1.1);
      color: #e6533c;
    }

    &.next {
      transform: rotate(180deg);

      &:hover {
        transform: scale(1.1) rotate(180deg);
      }
    }
  }
}
</style>
