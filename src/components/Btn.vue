<template>
  <div class="btn work" @click="$root.$emit('showForm')">
    Заказать работу
  </div>
</template>

<script>
export default {
  name: "Btn"
}
</script>

<style lang="scss" scoped>
.btn {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 48px;
  width: 193px;
  border-radius: 24px;
  background: #FE5806;
  cursor: pointer;

  &.work {
    font-weight: 600;
    font-size: 16px;
    line-height: 22px;
    color: #FFFFFF;
  }

  &:hover {
    background: #FE5806;
    opacity: 0.7;
    transition: 0.2s linear;
  }
}
</style>
