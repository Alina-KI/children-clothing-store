<template>
  <div class="imageBlock">
    <img class="image" v-bind:src="currentImage" alt="">
    <div class="listImage">
      <img class="smallImage" src="@/assets/images/14896420.jpg" @click="updateImage(require('@/assets/images/14896420.jpg'))" alt="">
      <img class="smallImage" src="@/assets/images/12296786.jpg" @click="updateImage(require('@/assets/images/12296786.jpg'))" alt="">
      <img class="smallImage" src="@/assets/images/13986707.jpg" @click="updateImage(require('@/assets/images/13986707.jpg'))" alt="">
      <img class="smallImage" src="@/assets/images/14896421.jpg" @click="updateImage(require('@/assets/images/14896421.jpg'))" alt="">
      <img class="smallImage" src="@/assets/images/12296786.jpg" @click="updateImage(require('@/assets/images/12296786.jpg'))" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: 'ImageBlock',
  data() {
    return {
      currentImage: require('@/assets/images/14896420.jpg')
    }
  },
  methods: {
    updateImage(currentImage) {
      this.currentImage = currentImage
    }
  }
}
</script>

<style scoped>
.imageBlock {
  position: relative;
  margin-left: 20px;
}

.image {
  width: 686px;
  height: 878px;
  object-fit: cover;
  position: relative;
}

.listImage {
  position: absolute;
  left: 21px;
  top: 26px;
  display: flex;
  flex-direction: column;
  gap: 7px;
}

.smallImage {
  width: 70px;
  height: 91px;
  position: relative;
}

@media (max-width: 1105px) {
  .imageBlock {
    margin: 0;
  }
}

@media (max-width: 1240px) {
  .image {
    width: 600px;
    height: 800px;
  }
}

@media (max-width: 1155px) {
  .image {
    width: 500px;
    height: 700px;
  }
}

@media (max-width: 530px) {
  .smallImage {
    width: 40px;
    height: 52px;
  }

  .image {
    width: 375px;
    height: 480px;
  }
}
</style>