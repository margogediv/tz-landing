<template>
  <div class="section-question">
    <div class="container">
      <h2 class="title">Остались вопросы?</h2>
      <div class="block-question">
        <div class="form">
          <div class="form-text">Оплата банковской картой</div>
          <div class="form-btn">
            <img src="./../assets/img/btn.svg" alt="">
          </div>
        </div>
        <div class="form">
          <div class="form-text">Оплата банковской картой</div>
          <div class="form-btn">
            <img src="./../assets/img/btn.svg" alt="">
          </div>
        </div>
        <div class="form">
          <div class="form-text">Оплата банковской картой</div>
          <div class="form-btn">
            <img src="./../assets/img/btn.svg" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: "TZQuestion"
}
</script>

<style lang="scss" scoped>
  .section-question {
    margin-bottom: 140px;

    .container {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      .title {
        font-weight: bold;
        font-size: 36px;
        line-height: 43px;
        color: #484C52;
        margin-bottom: 40px;
      }

      .block-question {
        display: flex;
        flex-direction: column;
        width: 100%;

        .form {
          display: flex;
          justify-content: space-between;
          align-items: center;
          max-width: 1170px;
          width: 100%;
          height: 72px;
          padding: 20px;
          background: #E9F6FB;
          border-radius: 20px;
          margin-bottom: 20px;

          &:last-child {
            margin-bottom: 0;
          }

          .form-text {
            font-family: 'Open Sans', sans-serif;
            font-weight: 600;
            font-size: 18px;
            line-height: 31px;
            color: #484C52;
          }

          .form-btn {
            width: 32px;
            height: 32px;
            background-size: cover;
            background-repeat: no-repeat;
            background-position: center;
          }
        }
      }
    }
  }
</style>
