<template>
  <div class="itemGallery">
    <img class="image" v-bind:src=image alt="">
    <div class="background">
      <div class="topBlock">
        <img src="@/assets/icons/FullScreen.svg" alt="">
      </div>
      <div class="middleBlock">
        <img src="@/assets/icons/BagWhite.svg" alt="">
        <span class="text">Узнай, что на мне</span>
      </div>
      <div class="bottomBlock">
        <img src="@/assets/icons/FavoriteFull.svg" alt="">
        <span class="text">200</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ItemGallery',
  props: {
    image: String,
  }
}
</script>

<style scoped>
.itemGallery {
  position: relative;
}

.image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.itemGallery:hover .background {
  display: flex;
}

.background {
  position: absolute;
  width: 100%;
  height: 100%;
  background: #333333;
  opacity: 0.7;
  inset: 0;
  display: none;
  flex-direction: column;
  justify-content: space-between;
  padding: 15px;
}

.topBlock {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-end;
}

.middleBlock {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.text {
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  color: #FFFFFF;
}

.bottomBlock {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
</style>