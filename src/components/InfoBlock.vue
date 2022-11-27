<template>
  <div class="infoBlock">
    <span class="title">Пижама для девочек</span>
    <span class="article">Арт. 02765/46</span>
    <div class="comment">
      <span>Отзывы</span>
      <div class="iconBlock">
        <img class="icon" src="@/assets/icons/Vector.svg" alt="">
        <img class="icon" src="@/assets/icons/Vector.svg" alt="">
        <img class="icon" src="@/assets/icons/Vector.svg" alt="">
        <img class="icon" src="@/assets/icons/Vector.svg" alt="">
        <img class="icon" src="@/assets/icons/Vector1.svg" alt="">
      </div>
      <span>14 отзывов</span>
      <img class="arrow" src="@/assets/icons/Arrow.svg" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: 'InfoBlock'
}
</script>

<style scoped>
.infoBlock {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.title {
  height: 32px;
  font-weight: 600;
  font-size: 18px;
  line-height: 24px;
  color: #333333;
}

.article {
  font-weight: 400;
  font-size: 12px;
  line-height: 16px;
  color: #828282;
  height: 28px;
}

.comment {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 5px;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  color: #333333;
  letter-spacing: 0.04em;
}

.iconBlock {
  display: flex;
  flex-direction: row;
}

.icon {
  width: 12px;
  height: 12px;
}
</style>