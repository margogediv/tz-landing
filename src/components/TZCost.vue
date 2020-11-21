<template>
  <div class="section-cost">
    <img class="cost-img" src="./../assets/img/cost-img.png" alt="">
    <div class="container">
      <h2 class="title-cost">Рассчитать стоимость</h2>
      <div class="form-cost">
        <div class="block-first">
          <div class="in-first select">
            <select v-model="form.typeWork.current">
              <option disabled value="0">Название работы</option>
              <option
                  v-for="item in form.typeWork.list"
                  :value="item.id"
              >{{ item.title }}</option>
            </select>
          </div>
          <div class="in-first select">
            <select v-model="form.nameSubject.current">
              <option disabled value="">Название предмета</option>
              <option
                  v-for="item in form.nameSubject.list"
              >{{ item }}</option>
            </select>
          </div>
          <input class="in-first" placeholder="Название темы"/>
          <input class="input-min" placeholder="Объем, стр."/>
          <div class="input-min">
            Срок сдачи
            <div class="calendar">
              <img src="./../assets/img/calendar2.svg" alt="">
            </div>
          </div>
        </div>
        <div class="block-second">
          <div class="input-form">
            <img src="./../assets/img/user-form.svg" alt="">
            <input class="user" placeholder="Ваше имя"/>
          </div>
          <div class="input-form">
            <input class="tel" placeholder="Номер телефона"/>
          </div>
          <div class="input-form">
            <img src="./../assets/img/email.svg" alt="">
            <input class="mail" placeholder="E-mail"/>
          </div>
          <div class="input-form">
            <img src="./../assets/img/promo.svg" alt="">
            <input class="promo" placeholder="Промокод"/>
          </div>
        </div>
        <div class="btn">Узнать стоимость</div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: "TZCost",
  data() {
    return {
      form: {
        typeWork: {
          current: 0,
          isOpen: false,
          list: []
        },
        nameSubject: {
          current: "",
          isOpen: false,
          list: []
        }
      },
    }
  },
  created() {
    this.getWorktypes();
    this.getSubjects();
  },
  methods: {
    openSelect(name) {
      this.form[name].isOpen = !this.form[name].isOpen;
    },
    setSelect(name, value) {
      this.form[name].current = value;
    },
    getWorktypes() {
      axios
          .get('https://zaochnik.com/rest/worktypes/')
          .then(response => {
            this.form.typeWork.list = response.data.results;
            console.log(response.data);
          })
          .catch(error => {
            console.log(error);
          })
    },
    getSubjects() {
      axios
          .get('https://zaochnik.com/api/get_subjects/')
          .then(response => {
            this.form.nameSubject.list = response.data;
          })
          .catch(error => {
            console.log(error);
          })
    }
  }
}
</script>

<style lang="scss" scoped>
.section-cost {
  max-width: 1920px;
  width: 100%;
  margin: 0 auto;
  position: relative;
  padding-top: 60px;
  background: #22A9D3;
  padding-bottom: 71px;

  .cost-img {
    position: absolute;
    top: 0;
    right: 0;
  }

  .container {
    .title-cost {
      font-weight: bold;
      font-size: 36px;
      line-height: 43px;
      color: #FFFFFF;
      margin-bottom: 40px;
    }

    .form-cost {
      max-width: 670px;
      width: 100%;
      z-index: 100;

      .block-first {
        display: flex;
        flex-wrap: wrap;

        max-width: 670px;
        width: 100%;

        margin-bottom: 20px;

        input {
          display: flex;
          align-items: center;

          width: 320px;
          height: 48px;

          background: #FFFFFF;
          border-radius: 40px;

          margin-right: 30px;
          margin-bottom: 20px;

          font-family: 'Open Sans', sans-serif;
          font-weight: normal;
          font-size: 14px;
          line-height: 24px;
          color: #484C52;
        }

        .in-first {
          margin-right: 30px;
          margin-bottom: 20px;
          width: 320px;
          height: 48px;
          background: #FFFFFF;
          border-radius: 40px;
          border: none;
          padding: 0 20px;
          font-family: 'Open Sans', sans-serif;
          font-weight: normal;
          font-size: 14px;
          line-height: 24px;
          color: #484C52;

          &:nth-child(2n+2) {
            margin-right: 0;
          }

        }

        .input-min {
          width: 150px;
          height: 48px;

          display: flex;
          align-items: center;
          justify-content: space-between;

          padding: 12px 20px;

          background: #FFFFFF;
          border-radius: 40px;

          margin-right: 20px;

          font-family: 'Open Sans', sans-serif;
          font-weight: normal;
          font-size: 14px;
          line-height: 24px;
          color: #484C52;

          &:last-child {
            margin-right: 0;
          }
        }
      }

      .block-second {
        display: flex;
        flex-wrap: wrap;

        max-width: 670px;
        width: 100%;

        margin-bottom: 10px;

        .input-form {
          width: 320px;
          height: 48px;

          display: flex;
          align-items: center;

          padding: 12px 20px;
          margin-right: 30px;
          margin-bottom: 23px;

          background: #FFFFFF;
          border-radius: 40px;

          input {
            width: 100%;
            font-family: 'Open Sans', sans-serif;
            font-weight: normal;
            font-size: 14px;
            line-height: 24px;
            color: #484C52;
            margin-left: 10px;
          }

          &:nth-child(2n+2) {
            margin-right: 0;
          }
        }
      }

      .btn {
        display: flex;
        align-items: center;
        justify-content: center;

        width: 212px;
        height: 48px;

        padding: 11px 30px;

        background: #FE5806;
        box-shadow: 0px 4px 12px rgba(236, 142, 95, 0.5);
        border-radius: 24px;

        font-family: 'Open Sans', sans-serif;
        font-weight: 600;
        font-size: 16px;
        line-height: 22px;
        color: #FFFFFF;
        cursor: pointer;

        &:hover {
          background: #F88850;
          transition: 0.2s linear;
        }
      }
    }
  }
}

.select {
  position: relative;
  padding: 0;

  select {
    height: 100%;
    width: 100%;
    border: none;
    font: inherit;
    color: inherit;
    background: inherit;
    padding: 0 20px;
    border-radius: inherit;
    -webkit-appearance: none;
    -moz-appearance: none;
    text-indent: 1px;
    text-overflow: '';
  }

  option[disabled="disabled"] {
    background: #e1dbdb;
  }

  &::before {
    content: "";
    display: block;
    background-image: url('./../assets/img/arrom-min.svg');
    background-repeat: no-repeat;
    background-size: 100%;
    width: 10px;
    height: 6px;
    position: absolute;
    top: 50%;
    right: 20px;
    transform: translateY(-50%);
    z-index: 1;
  }
}

</style>
