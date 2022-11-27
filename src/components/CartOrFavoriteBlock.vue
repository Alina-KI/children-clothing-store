<template>
  <div class="addCartOrFavorite">
    <div class="block">
      <div class="counterBlock">
        <button class="incrementDecrement" @click="increment">+</button>
        <span>{{this.count}}</span>
        <button class="incrementDecrement" @click="decrement">-</button>
      </div>
      <div class="cartFavoriteBlock">
        <button @click="openModal(true)" class="addCart">Добавить в корзину</button>
        <button @click="openModal(false)" class="favorite">
          <img src="@/assets/icons/FavoriteWhite.svg" alt="">
        </button>
      </div>
    </div>
    <button class="buyButton">Купить в 1 клик</button>
    <Popover ref="modal" :count-product="count" :is-show="showModal" :is-cart="isCart" title-product="Пижама для девочек"/>
  </div>
</template>

<script>
import Popover from '@/components/Popover'
export default {
  name: 'CartOrFavoriteBlock',
  components: { Popover },
  data() {
    return {
      count: 1,
      showModal: false,
      isCart: false
    }
  },
  methods: {
    increment() {
      this.count++
    },
    decrement() {
      if (this.count > 1) {
        this.count--
      }
    },
    openModal(isCart) {
      this.isCart = isCart
      this.$refs.modal.show()
    }
  }
}
</script>

<style scoped>
.addCartOrFavorite {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.block {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: center;
  gap: 10px;
}

.cartFavoriteBlock {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: center;
  gap: 5px;
}

.counterBlock {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  background: #F2F2F2;
  padding: 15px;
  gap: 40px;
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  color: #333333;
  height: 44px;
}

.incrementDecrement {
  background: transparent;
  border: none;
  outline: none;
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  color: #333333;
}

.addCart {
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  color: #FFFFFF;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 8px 28px;
  gap: 10px;
  background: #333333;
  border: 1px solid #333333;
  height: 44px;
}

.favorite {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  width: 44px;
  height: 44px;
  background: #333333;
  border: 1px solid #333333;
}

.buyButton {
  background: transparent;
  text-align: start;
  border: none;
  outline: none;
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  text-decoration-line: underline;
  color: #333333;
}
</style>