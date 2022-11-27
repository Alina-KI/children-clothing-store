<template>
  <div class="product">
    <div class="container">
      <div class="block">
        <ImageBlock />
        <div class="info">
          <ProductInfo />
          <div class="line" />
          <AdditionalInfo />
        </div>
      </div>
      <a class="link" href="#">Посмотреть все стили</a>
      <Gallery />
    </div>
  </div>
</template>

<script>
import Gallery from '@/components/Gallery'
import ProductInfo from '@/components/ProductInfo'
import AdditionalInfo from '@/components/AdditionalInfo'
import ImageBlock from '@/components/ImageBlock'

export default {
  name: 'Product',
  components: { ImageBlock, AdditionalInfo, ProductInfo, Gallery }
}
</script>

<style scoped>
.product {
  max-width: 1390px;
  width: 100%;
  margin: 0 auto;
}

.container{
  display: flex;
  flex-direction: column;
  gap: 30px;
  margin-bottom: 130px;
  margin-top: 25px;
}

.block {
  display: flex;
  flex-direction: row;
  gap: 15px;
  flex-wrap: wrap;
}

.info {
  display: flex;
  flex-direction: column;
  gap: 25px;
}

.line {
  width: 100%;
  height: .5px;
  background: #C4C4C4;
}

.link{
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.04em;
  text-decoration-line: underline;
  color: #333333;
}

@media (max-width: 1105px) {
  .block {
    justify-content: center;
  }
  .info{
    width: 100%;
  }
}
@media (min-width: 1105px) {
  .line{
    max-width: 686px;
  }
}
@media (min-width: 1105px) {
  .info{
    min-width: 500px;
  }
}
</style>