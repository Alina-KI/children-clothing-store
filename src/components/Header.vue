<template>
  <div class="header">
    <div class="container">
      <img class="logo" src="@/assets/icons/Logo.svg" alt="" />
      <div class="blockImages">
        <button class="buttonImage">
          <img src="@/assets/icons/Person.svg" alt="">
        </button>
        <button class="buttonImage">
          <img src="@/assets/icons/Favorite.svg" alt="">
        </button>
        <button class="buttonImage">
          <img src="@/assets/icons/Bag.svg" alt="">
        </button>
        <button class="buttonImage" @click="show = !show">
          <img class="menu" src="@/assets/icons/Menu.svg" alt="">
        </button>
      </div>
    </div>
    <Transition name="slide-fade">
      <div v-if="show" class="burgerMenu">
        <button class="buttonImage" @click="show = !show">
          <img class="cross" src="@/assets/icons/Cross.svg" alt="">
        </button>
        <a class="link" href="#">постельное белье</a>
        <a class="link" href="#">одежда для дома</a>
        <a class="link" href="#">Одежда для улицы</a>
        <a class="link" href="#">Выход</a>
      </div>
    </Transition>
  </div>
</template>

<script lang="ts">

export default {
  name: 'Header',
  data() {
    return {
      show: false
    }
  }

}
</script>

<style scoped>
.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateY(-20px);
  opacity: 0;
}

.header {
  position: relative;
  display: flex;
  flex-direction: row;
  height: 60px;
  padding: 0 20px;
  width: 100%;
}

.container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  max-width: 1390px;
  width: 100%;
  margin: 0 auto;
}

.blockImages {
  flex-grow: 1;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-end;
  gap: 25px;
}

.buttonImage {
  background: transparent;
  border: none;
  outline: none;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}

.logo {
  width: 67px;
  height: 16px;
}

.menu {
  width: 24px;
  height: 24px;
  display: block;
}


.burgerMenu {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 80px 20px 30px 30px;
  gap: 30px;
  background: #FFFFFF;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  z-index: 2;
  scroll-behavior: smooth;
  transition: all .3s ease;
}

.cross {
  position: absolute;
  width: 24px;
  height: 24px;
  right: 20px;
  top: 18px;
  z-index: 3;
}

.link {
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 16px;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: #333333;
  text-decoration: none;
  scroll-behavior: smooth;
}

@media (min-width: 800px) {
  .header {
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    height: 40px;
  }

  .logo {
    width: 64px;
    height: 16px;
  }

  .menu {
    display: none;
  }
}
</style>