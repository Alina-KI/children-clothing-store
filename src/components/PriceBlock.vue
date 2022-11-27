<template>
  <div class="price">
    <div class="block">
      <div class="priceBlock">
        <span class="currentPrice">800 ₽</span>
        <span class="oldPrice">1 500 ₽</span>
        <img src="@/assets/icons/Arrow.svg" alt="" class="arrow">
      </div>
      <div class="discountBlock">
        <span class="discount">скидка -36%</span>
        <span class="discount">акция -20%</span>
      </div>
    </div>
    <div class="sizesBlock">
      <ComboBox/>
      <a href="#" class="determineSize">Определить размер</a>
    </div>
  </div>
</template>

<script>
import ComboBox from '@/components/ComboBox'
export default {
  name: 'PriceBlock',
  components: { ComboBox }
}
</script>

<style scoped>
.price {
  display: flex;
  flex-direction: column;
  gap: 30px;
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
}

.block {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.priceBlock {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  gap: 10px;
}

.currentPrice {
  font-weight: 700;
  font-size: 24px;
  line-height: 24px;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: #333333;
}

.oldPrice {
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  text-decoration-line: line-through;
  color: #828282;
}

.arrow {

}

.discountBlock {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  gap: 10px;
}

.discount {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 4px 8px;
  font-weight: 400;
  font-size: 12px;
  line-height: 16px;
  letter-spacing: 0.04em;
  color: #333333;
  border: 1px solid #333333;

}

.sizesBlock {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
}

.sizes {
  height: 44px;
}
.determineSize{
  height: 28px;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  text-decoration-line: underline;
  color: #333333;
}
</style>