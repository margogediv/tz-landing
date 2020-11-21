<template>
  <div>
    <div class="section-couse">
      <div class="group">
        <div class="box"></div>
        <img class="img-mac" src="./../assets/img/MacBook.png" alt="">
      </div>
      <div class="couse-text">
        <h2 class="title">
          <span>Zaochnik</span>
          отличается <br> потому что
          <img class="ic" src="./../assets/img/ic.svg" alt="">
        </h2>
        <ul class="list">
          <li class="iteam first">Сразу несколько экспертов будут заниматься твоей задачей, и даже если кто-то заболеет, мы оперативно заменим слабое звено</li>
          <li class="iteam second">Толпа корректоров выверит каждую букву и проверит работу на уникальность</li>
          <li class="iteam last">Служба поддержки ответит в любое время дня и ночи по любому каналу связи</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: "TZCouse"
}
</script>

<style lang="scss" scoped>
  .section-couse {
    max-width: 1920px;
    width: 100%;
    margin: 0 auto;
    height: auto;
    position: relative;
    display: flex;
    margin-bottom: 170px;

    .group {
      width: 960px;
      height: auto;
      .box {
        width: 745px;
        height: 489px;
        background-color:  #22A9D3;;
        left: 0;
        top: 0;
      }

      .img-mac {
        position: absolute;
        top: 0;
      }
    }

     .couse-text {
       width: 570px;
       padding-top: 67px;
       padding-right: 20px;
       span {
         font-weight: 900;
         font-size: 36px;
         line-height: 43px;
         color: #22A9D3;;
       }
       .title {
         position: relative;
         font-weight: 900;
         font-size: 36px;
         line-height: 43px;
         color: #484C52;
         margin-bottom: 29px;

         .ic {
           position: absolute;
           top: -69px;
           right: 64px;
         }
       }

       .list {
         display: flex;
         flex-direction: column;
         align-items: center;
         .iteam {
           height: 103px;

           position: relative;

           display: flex;
           align-items: center;
           padding-left: 104px;

           font-weight: 600;
           font-size: 16px;
           line-height: 22px;
           color: #6D7075;

           &.first:before {
             position: absolute;
             top: 0;
             left: 0;

             display: flex;
             content: '';
             width: 103px;
             height: 103px;

             background-image: url("./../assets/img/1.svg");
             background-size: cover;
             background-repeat: no-repeat;
             background-position: center;

           }

           &.second:before {
             position: absolute;
             top: 0;
             left: 0;

             display: flex;
             content: '';
             width: 103px;
             height: 103px;

             background-image: url("./../assets/img/2.svg");
             background-size: cover;
             background-repeat: no-repeat;
             background-position: center;

           }

           &.last:before {
             position: absolute;
             top: 0;
             left: 0;

             display: flex;
             content: '';
             width: 103px;
             height: 103px;

             background-image: url("./../assets/img/3.svg");
             background-size: cover;
             background-repeat: no-repeat;
             background-position: center;

           }
         }
       }
     }
   }
</style>
