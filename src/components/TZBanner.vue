<template>
  <div>
    <div class="section-banner">
      <div class="container">
        <div class="block">
          <div class="block-left">
            <h2 class="title">
              Скорая помощь<br> для студента
              <img class="ic" src="./../assets/img/ic.svg" alt="">
            </h2>
            <div class="subtitle">Zaochnik помогает в самых сложных ситуациях </div>
            <div class="resul-work">
              <div class="consultation">
                <div class="title-name">Провели</div>
                <div class="view">1 500 000+</div>
                <div class="subtitle-name">консультаций</div>
              </div>
              <div class="work">
                <div class="title-name">Написали</div>
                <div class="view">1 100 000+</div>
                <div class="subtitle-name">работ</div>
              </div>
            </div>
            <Btn/>
          </div>
          <div class="block-right">
            <img src="./../assets/img/banner.jpg" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Btn from "./Btn";
export default {
name: "TZBanner",
  components: {Btn}
}
</script>

<style lang="scss" scoped>
 .section-banner {
   max-width: 1920px;
   width: 100%;
   margin: 0 auto;
   height: auto;
   background: #E9F6FB;
   .container {
     display: flex;
     .block {
       width: 100%;
       display: flex;
       justify-content: space-between;
       .block-left {
         width: 450px;
         height: auto;

         padding-top: 104px;
         padding-bottom: 97px;


         .title {
           position: relative;
           font-weight: bold;
           font-size: 40px;
           line-height: 47px;
           color: #484C52;
           margin-bottom: 32px;

           .ic {
             position: absolute;
             top: -69px;
             right: 29px;
           }
         }

         .subtitle {
           font-family: 'Open Sans' , sans-serif;
           font-weight: 600;
           font-size: 18px;
           line-height: 23px;
           color: #6D7075;
           margin-bottom: 32px;
         }

         .resul-work {
           width: 100%;
           display: flex;
           margin-bottom: 42px;

           .consultation,
           .work {
             .title-name {
               color: #22A9D3;
               font-weight: 600;
               font-size: 18px;
               line-height: 23px;
               margin-bottom: 8px;
             }

             .view {
               font-size: 40px;
               font-weight: 700;
               margin-bottom: 10px;
               color: #484C52;
             }

             .subtitle-name {
               font-weight: 600;
               font-size: 18px;
               line-height: 23px;
               margin-bottom: 8px;
               color: #828282;
             }
           }

           .consultation {
             margin-right: 40px;
           }
         }
       }
     }
   }
 }
</style>
