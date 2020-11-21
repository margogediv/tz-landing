<template>
<div>
  <div class="section-servis">
    <div class="container">
      <h2 class="title">Наш сервис максимально прост</h2>
      <ul class="list">
        <li class="iteam">
          <img src="./../assets/img/icons-1.svg" alt="">
          <div class="subtitle">Прием заявки</div>
        </li>
        <li class="iteam">
          <img src="./../assets/img/icons-2.svg" alt="">
          <div class="subtitle">Оценка стоимости</div>
        </li>
        <li class="iteam">
          <img src="./../assets/img/icons-3.svg" alt="">
          <div class="subtitle">
            Внесение<br>
            предоплаты 25%
          </div>
        </li>
        <li class="iteam">
          <img src="./../assets/img/icons-4.svg" alt="">
          <div class="subtitle">Выполнение заказа</div>
        </li>
        <li class="iteam">
          <img src="./../assets/img/icons-5.svg" alt="">
          <div class="subtitle">Сдача работы</div>
        </li>
      </ul>
    </div>
  </div>
</div>
</template>

<script>
export default {
name: "TZServis"
}
</script>

<style lang="scss" scoped>
.section-servis {
  margin-bottom: 106px;
  .container {
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    .title {
      font-weight: bold;
      font-size: 36px;
      line-height: 43px;
      color: #484C52;
      margin-bottom: 37px;
    }

    .list {
      width: 100%;
      height: auto;
      display: flex;
      align-items: center;
      justify-content: center;
      .iteam {

        margin-right: 80px;
        position: relative;

        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;

        &:last-child::before {
          display: none;
        }

        img {
          width: 148px;
          height: 148px;
        }

        &:before {
          content: '';
          width: 30px;
          height: 15px;

          position: absolute;
          top: 40%;
          right: -60px;
          transform: translateY(-50%);

          background-image: url("./../assets/img/arrow.svg");
          background-position: center;
          background-repeat: no-repeat;
          background-size: cover;
        }

        .subtitle {
          text-align: center;
          width: 100%;
          font-family: "Open Sans", sans-serif;
          font-weight: bold;
          font-size: 16px;
          line-height: 22px;
          color: #484C52;
        }
      }
    }
  }
}
</style>
