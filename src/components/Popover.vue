<template>
  <Transition name="slide-fade">
    <div v-if="showModal" class="modal">
      <button class="close" @click="hide">
        <img class="cross" src="@/assets/icons/Cross.svg" alt="">
      </button>
      <span class="text">
      Товар {{ titleProduct }} в количестве {{ countProduct }} единиц добавлен в {{ isCart ? 'корзину' : 'избранное' }}.
    </span>
    </div>
  </Transition>
</template>

<script>
export default {
  name: 'Popover',
  data() {
    return {
      showModal: false
    }
  },
  props: {
    titleProduct: String,
    countProduct: String,
    isCart: Boolean
  },
  methods: {
    show() {
      this.showModal = true
    },
    hide(){
      this.showModal = false
    }
  }
}
</script>

<style scoped>
.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.3s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateY(20px);
  opacity: 0;
}

.modal {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  max-width: 370px;
  height: 150px;
  padding: 10px 15px;
  background: #FFFFFF;
  box-shadow: 4px 7px 8px rgba(0, 0, 0, 0.3), 0 -3px 10px rgba(0, 0, 0, 0.2);
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  border-radius: 10px;
  z-index: 2;
}

.close {
  position: absolute;
  z-index: 3;
  top: 10px;
  right: 10px;
  background: transparent;
  border: none;
  outline: none;
}

.cross {
  width: 24px;
  height: 24px;
}

.text {
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 24px;
  color: #333333;
}
</style>