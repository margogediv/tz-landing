<template>
  <div>
    <div class="section-guarantee">
      <div class="img-block"></div>
      <div class="text-block">
        <div class="box">
          <h2 class="title">
            Гарантии сервиса
            <div>Zaochnik</div>
            <img class="ic" src="./../assets/img/ic.svg" alt="">
          </h2>
          <ul class="service">
            <li class="service-item">
              <span>Честная цена</span> подразумевает адекватное <br> сочетание цена/качество
            </li>
            <li class="service-item">
              <span>Соблюдение конфиденциальности</span> не допускает <br> передачу ваших данных третьим лицам
            </li>
            <li class="service-item">
              Договор оферты и гарантия возврата средств <br> позволяет <span>минимизировать риски</span>
            </li>
          </ul>
          <Btn />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Btn from "./Btn";

export default {
  name: "TZGuarantee",
  components: {
    Btn,
  },
}
</script>

<style lang="scss" scoped>

  .section-guarantee {
    max-width: 1920px;
    width: 100%;
    margin: 0 auto;
    display: flex;
    margin-bottom: 122px;

    .img-block {
      width: 50%;

      background-image: url("./../assets/img/service.jpg");
      background-position: center;
      background-repeat: no-repeat;
      background-size: cover;
    }

    .text-block {
      width: 50%;
      display: flex;
      flex-direction: column;
      background: #E9F6FB;

      .box {
        height: auto;
        margin-left: 133px;
        padding-top: 92px;
        padding-bottom: 130px;
        .title {
          position: relative;
          width: 550px;
          font-weight: 900;
          font-size: 36px;
          line-height: 43px;
          color: #484C52;
          margin-bottom: 40px;

          div {
            font-weight: 900;
            font-size: 36px;
            line-height: 43px;
            color: #22A9D3;;
          }

          .ic {
            position: absolute;
            top: -69px;
            right: 96px;
          }
        }
        .service {
          display: flex;
          flex-direction: column;
          .service-item {
            position: relative;
            font-family: 'Open Sans', sans-serif;
            font-weight: normal;
            font-size: 18px;
            line-height: 31px;
            color: #333333;
            margin-bottom: 13px;

            span {
              font-family: 'Open Sans', sans-serif;
              font-weight: bold;
              color: #333333;
            }

            &:before {
              content: '';
              position: absolute;
              top: 6px;
              left: -32px;

              width: 18px;
              height: 18px;

              background-image: url("./../assets/img/icon-ok.svg");
              background-size: cover;
              background-repeat: no-repeat;
              background-position: center;
            }
          }
        }
      }
    }
  }
</style>
