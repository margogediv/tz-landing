<template>
  <div class="overlay">
    <div class="modal-created">
      <div class="form">
        <div class="form-header">
          <img
              class="close"
              @click="$root.$emit('changeshowTZForm')"
              src="./../assets/img/close.svg"
              alt="">
        </div>
        <div class="form-check">
          <img src="./../assets/img/cheack.svg" alt="">
        </div>
        <div class="form-body">
          <div class="title">Спасибо!</div>
          <div class="subtitle">Ваша заявка принята</div>
        </div>
        <div class="form-footer">
          <div
              class="btn"
              @click="$root.$emit('changeshowTZForm')"
           >
            Текст кнопки
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>


export default {
  name: "TZForm",

}
</script>

<style lang="scss" scoped>

.overlay {
  width: 100%;
  height: 100%;
  position: fixed;
  z-index: 19;
  top: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.54);
}

.modal-created {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);

  max-width: 570px;
  width: 100%;
  height: 341px;

  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;

  background: #FFFFFF;
  border-radius: 20px;

  .form {
    padding: 20px;
    width: 100%;
    height: auto;

    .form-header {
      position: relative;

      .close {
        position: absolute;
        top: 0;
        right: 0;
        cursor: pointer;
      }
    }
    .form-check {
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      padding-top: 40px;
      margin-bottom: 24px;
    }
    .form-body {
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;

      .title {
        font-weight: bold;
        font-size: 30px;
        line-height: 34px;
        color: #22A9D3;
        margin-bottom: 16px;
      }

      .subtitle {
        font-weight: bold;
        font-size: 24px;
        line-height: 27px;
        color: #484C52;
        margin-bottom: 30px;
      }
    }
    .form-footer {
      display: flex;
      align-items: center;
      justify-content: center;
      .btn {
        width: 193px;
        height: 48px;

        display: flex;
        align-items: center;
        justify-content: center;

        padding: 11px 30px;
        background: #FE5806;
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


</style>
