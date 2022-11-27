<template>
  <div class="footer">
    <div class="smallBlock">
      <span class="title">покупателям</span>
      <div class="linkBlock">
        <a class="link" href="#">Каталог</a>
        <a class="link" href="#">Акции</a>
        <a class="link" href="#">Бренды</a>
      </div>
    </div>
    <div class="smallBlock">
      <span class="title">о нас</span>
      <div class="linkBlock">
        <a class="link" href="#">О компании</a>
        <a class="link" href="#">Новости</a>
        <a class="link" href="#">Команда</a>
      </div>
    </div>
    <form class="block">
      <span class="title">Узнайте первыми о новинках и акциях</span>
      <div class="blockMail">
        <input class="mail" type="email" placeholder="Адрес электронной почты" v-model="email">
        <button v-if="email.length > 0" class="clear" @click="clearMail">
          <img class="icon" src="@/assets/icons/Cross.svg" alt="">
        </button>
      </div>
      <button class="subscribe">Подписаться</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return{
      email: ''
    }
  },
  methods: {
    clearMail() {
      this.email = ''
    }
  }
}
</script>

<style scoped>
.footer {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-around;
  padding: 0 20px;
  column-gap: 10px;
  row-gap: 30px;
  margin-bottom: 70px;
}

.block {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: flex-start;
  gap: 15px;
}

.smallBlock{
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: flex-start;
  gap: 15px;
}

.linkBlock {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  max-width: 170px;
  gap: 7px;
}

.title{
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: #333333;
  width: 100%;
  text-align: start;
}
.link{
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  color: #333333;
  text-decoration: none;
  min-width: 150px;
  text-align: start;
}

.blockMail{
  position: relative;
  width: 100%;
  height: 44px;
}

.clear{
  position: absolute;
  top: 15px;
  right: 15px;
  background: transparent;
  border: none;
  outline: none;
  width: 16px;
  height: 16px;
}

.icon{
  width: 16px;
  height: 16px;
}

.mail{
  width: 100%;
  height: 44px;
  border: none;
  border-bottom: 1px solid #C4C4C4;
  outline: none;
  padding: 12px 14px;
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  color: #828282;
}

.subscribe{
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 8px 28px;
  gap: 10px;
  background: #FFFFFF;
  border: 1px solid #333333;
  outline: none;
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  color: #333333;
}

@media (max-width: 600px) {
  .footer{
    column-gap: 30px;
  }
  .block{
    width: 100%;
    align-items: flex-start;
  }
  .title{
    max-width: 255px;
  }

}
</style>