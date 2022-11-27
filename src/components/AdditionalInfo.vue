<template>
  <div class="additionalInfo">
    <div class="infoBlock">
      <img class="icon" src="@/assets/icons/Closes.svg" alt="">
      <a href="#" class="text">Описание товара</a>
    </div>
    <div class="infoBlock">
      <img class="icon" src="@/assets/icons/Clock.svg" alt="">
      <a href="#" class="text">Доставка и возврат</a>
    </div>
    <div class="infoBlock">
      <img class="icon" src="@/assets/icons/Pay.svg" alt="">
      <a href="#" class="text">Способы оплаты</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'additionalInfo'
}
</script>

<style scoped>
.additionalInfo {
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 0 20px;
}

.infoBlock {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  gap: 5px;
}

.icon {
  width: 20px;
  height: 20px;
}

.text {
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  text-decoration-line: underline;
  color: #333333;
}

@media (max-width: 1105px) {
  .additionalInfo{
    max-width: 500px;
    width: 100%;
    margin: 0 auto;
  }
}
</style>