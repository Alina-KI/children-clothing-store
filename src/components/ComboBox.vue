<template>
  <div class="comboBox">
    <div class="inputBlock">
      <input type="text" class="input" placeholder="Выбрать размер" />
      <img class="arrow" src="@/assets/icons/Arrow.svg" alt="">
    </div>
<!--    <ul class="listBlock">-->
<!--      <li v-for="item in items" v-bind:key="item" class="itemList">-->
<!--        {{ item }}-->
<!--      </li>-->
<!--    </ul>-->
  </div>
</template>

<script>
export default {
  name: 'ComboBox',
  data() {
    return {
      items: ['17', '18', '19', '20']
    }
  }
}
</script>

<style scoped>
.comboBox {
  position: relative;
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  color: #333333;
}

.inputBlock {
  position: relative;
  border: 1px solid #333333;
  padding: 12px 16px;
  width: 315px;
}

.input {
 font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  color: #333333;
  width: 100%;
  height: 100%;
  border: none;
  outline: none;
}

.input::placeholder {
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  color: #333333;
}

.arrow {
  position: absolute;
  width: 24px;
  height: 24px;
  right: 8px;
  top: 10px;
  transform: rotateZ(90deg);
}

.arrowActive {
  transform: rotateZ(270deg);
}

.listBlock{
  position: absolute;
  left: 0;
  right: 0;
  padding-top: 10px;
  background: #FFFFFF;
  border: 1px solid #333333;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

.itemList{
  list-style-type: none;
  width: 100%;
  height: 25px;
  font-size: 16px;
  border-bottom: 1px solid #333333;
}
</style>