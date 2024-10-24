<template>
  <div>
    <div class="blocks">
      <div>
        <h2>Тренируйтесь дома</h2>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Expedita
          voluptatum ut odio debitis eaque excepturi vitae dolorem optio libero,
          consectetur nostrum veritatis molestias quae fuga, illo, assumenda eum
          nulla soluta eos saepe! Facilis doloribus quidem voluptates minus
          vitae, excepturi praesentium reprehenderit eos reiciendis. Omnis
          dolore numquam itaque, blanditiis consectetur quidem?
        </p>
        <span
          ><a href="#!">Больше</a> <i class="fa-solid fa-arrow-right"></i
        ></span>
      </div>
      <div>
        <img src="/img/info-1.png" alt="" />
      </div>
      <div>
        <img src="/img/info-2.png" alt="" />
      </div>
      <div>
        <h2>Получите еще <br />больше эксклюзивного <br />контента</h2>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident
          obcaecati officiis cupiditate corporis hic tenetur veniam voluptatum
          possimus molestias? Nulla, nihil exercitationem unde itaque illo non
          cupiditate totam possimus odio.
        </p>
        <span
          ><a href="#!">Больше</a> <i class="fa-solid fa-arrow-right"></i
        ></span>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.blocks {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  margin-top: 80px;

  @media (max-width: 1100px) {
    flex-direction: column;
  }

  > div {
    @media (min-width: 900px) {
      width: 50%;
    }

    h2 {
      margin-bottom: 30px;
      font-size: 2.2em;
    }

    p {
      color: #9b9a97;
      max-width: 450px;
      margin-bottom: 20px;
    }

    span {
      a {
        color: #e6533c;

        &:hover {
          color: #fff;
        }
      }
      i {
        margin-left: 15px;
        font-size: 1.2em;
        cursor: pointer;
        transition: all 600ms ease;

        &:hover {
          transform: translateY(10px);
        }
      }
    }

    img {
      max-width: 90%;

      @media (max-width: 1100px) {
        &:first-of-type {
          margin-top: 30px;
        }
      }
    }
  }
}
</style>
