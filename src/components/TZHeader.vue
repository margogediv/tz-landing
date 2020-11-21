<template>
  <div>
    <div class="section-header">
      <div class="container">
        <div class="logo">
          <img class="logo-img" src="./../assets/img/logo.png">
        </div>
        <div class="workOrder">
          <div class="phone">
            <div class="icon">
              <img class="icon-img" src="./../assets/img/iconPhone.svg">
            </div>
            <div class="tel">
              <div class="tel-number">8 801 802 03 04</div>
              <div class="tel-text">Заказать звонок?</div>
            </div>
          </div>
          <Btn />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Btn from "./Btn";

export default {
  name: 'TZHeader',
  components: {
    Btn
  },
}
</script>

<style scoped lang="scss">
 .section-header {
   max-width: 1920px;
   width: 100%;
   margin: 0 auto;
   height: 88px;
   background: #FFFFFF;
   box-shadow: 0px 0px 20px rgba(52, 65, 84, 0.1);

   .container {
     display: flex;
     justify-content: space-between;
     .logo {
       padding-top: 24px;
       padding-bottom: 24px;

       .logo-img {
         width: 129px;
         height: 40px;
         cursor: pointer;
       }
     }
     .workOrder {
       display: flex;
       align-items: center;
       .phone {
         display: flex;
         margin-right: 85px;
         .icon {
           margin-right: 8px;
         }
         .tel {
           .tel-number {
             font-weight: bold;
             font-size: 20px;
             line-height: 23px;
             color: #484C52;
           }
           .tel-text {
             font-weight: normal;
             font-size: 12px;
             line-height: 20px;
             color: #FE5806;
             cursor: pointer;

             &:hover {
               text-decoration: underline;
               transition: 0.2s linear;
             }
           }
         }
       }
     }
   }
 }
</style>
