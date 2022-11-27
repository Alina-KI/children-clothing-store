<template>
  <div class="gallery">
    <ItemGallery class="image" :image="require('@/assets/images/12296786.jpg')"/>
    <div class="blockImage">
      <ItemGallery class="smallImage" :image="require('@/assets/images/14896420.jpg')"/>
      <ItemGallery class="smallImage" :image="require('@/assets/images/13986707.jpg')"/>
      <ItemGallery class="smallImage" :image="require('@/assets/images/14896421.jpg')"/>
      <ItemGallery class="smallImage" :image="require('@/assets/images/12296786.jpg')"/>
    </div>
  </div>
</template>

<script>
import ItemGallery from '@/components/ItemGallery'
export default {
  name: 'Gallery',
  components: { ItemGallery }
}
</script>

<style scoped>
.gallery {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: center;
  align-items: center;
  gap: 15px;
}

.image {
  max-width: 686px;
  max-height: 688px;
}

.image:hover, .smallImage:hover{
  cursor: pointer;
}

.blockImage {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 15px;
}

.smallImage {
  width: 335px;
  height: 336px;
}

@media (max-width: 1420px) {
  .gallery {
    flex-wrap: wrap;
  }

  .blockImage {
    width: 686px;
  }
}

@media (max-width: 690px) {
  .blockImage {
    width: 380px;
    gap: 5px;
  }

  .image {
    width: 375px;
    height: 375px;
  }

  .smallImage {
    width: 180px;
    height: 180px;
  }
}
</style>