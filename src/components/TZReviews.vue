<template>
  <div class="section-reviews">
    <div class="container">
      <h2 class="title-reviews">О нас говорят</h2>
      <div class="block-reviews">
        <div class="form-reviews">
          <div class="header">
            <div class="icon">
              <img src="./../assets/img/user.svg" alt="">
            </div>
            <div class="box-data">
              <div class="name">Имя Фамилия</div>
              <div class="date">24.12.2018</div>
            </div>
            <div class="quotes"></div>
          </div>
          <div class="body-text">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi aut maxime aliquam, nobis pariatur omnis officiis, non rem harum quia eligendi.
            <div class="play"></div>
          </div>
        </div>
        <div class="form-reviews">
          <div class="header">
            <div class="icon">
              <img src="./../assets/img/user2.svg" alt="">
            </div>
            <div class="box-data">
              <div class="name">Имя Фамилия</div>
              <div class="date">24.12.2018</div>
            </div>
            <div class="quotes"></div>
          </div>
          <div class="body-text">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi aut maxime aliquam, nobis pariatur omnis officiis, non rem harum quia eligendi.
            <div class="play"></div>
          </div>
        </div>
        <div class="form-reviews">
          <div class="header">
            <div class="icon">
              <img src="./../assets/img/user.svg" alt="">
            </div>
            <div class="box-data">
              <div class="name">Имя Фамилия</div>
              <div class="date">24.12.2018</div>
            </div>
            <div class="quotes"></div>
          </div>
          <div class="body-text">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi aut maxime aliquam, nobis pariatur omnis officiis, non rem harum quia eligendi.
            <div class="play"></div>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
name: "TZReviews"
}
</script>

<style lang="scss" scoped>
  .section-reviews {
    width: 100%;
    margin-bottom: 127px;

    .container {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      .title-reviews {
        font-weight: bold;
        font-size: 36px;
        line-height: 43px;
        color: #484C52;

        margin-bottom: 42px;
      }

      .block-reviews {
        display: flex;
        align-items: center;
        justify-content: center;

        .form-reviews {
          margin-right: 30px;

          width: 370px;
          height: 231px;
          padding: 20px;

          background: #FFFFFF;
          box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.1);
          border-radius: 12px;

          &:last-child {
            margin-right: 0;
          }

          .header {
            display: flex;
            position: relative;
            margin-bottom: 26px;

            .icon {
              width: 60px;
              height: 60px;
            }

            .box-data {
              margin-left: 10px;

              .name {
                font-family: 'Open Sans', sans-serif;
                font-weight: 600;
                font-size: 18px;
                line-height: 23px;
                color: #484C52;
                margin-bottom: 8px;
              }

              .date {
                position: relative;
                font-family: 'Open Sans', sans-serif;
                font-weight: normal;
                font-size: 12px;
                line-height: 16px;
                color: #4F4F4F;
                padding-left: 16px;

                &:before {
                  content: '';

                  position: absolute;
                  top: 0;
                  left: 0;

                  width: 13px;
                  height: 14px;

                  background-image: url("./../assets/img/calendar.svg");
                  background-size: cover;
                  background-repeat: no-repeat;
                  background-position: center;
                }
              }
            }

            .quotes {
              display: flex;

              position: absolute;
              top: 0;
              right: 0;

              width: 24px;
              height: 18px;

              background-image: url("./../assets/img/quotes.svg");
              background-size: cover;
              background-repeat: no-repeat;
              background-position: center;
            }
          }

          .body-text {
            position: relative;
            font-family: 'Open Sans', sans-serif;
            font-weight: normal;
            font-size: 14px;
            line-height: 24px;
            color: #828282;

            .play {
              display: flex;

              position: absolute;
              bottom: -13px;
              right: 0;

              width: 32px;
              height: 27px;

              background-image: url("./../assets/img/play.svg");
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
