<template>
  <div class="infoProduct">
    <InfoBlock />
    <PriceBlock />
    <CartOrFavoriteBlock />
  </div>
</template>

<script>
import PriceBlock from '@/components/PriceBlock'
import InfoBlock from '@/components/InfoBlock'
import CartOrFavoriteBlock from '@/components/CartOrFavoriteBlock'
import AdditionalInfo from '@/components/AdditionalInfo'

export default {
  name: 'ProductInfo',
  components: { CartOrFavoriteBlock, InfoBlock, PriceBlock }
}
</script>

<style scoped>
.infoProduct {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 40px;
  align-items: flex-start;
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  padding: 0 20px;
}
@media (max-width: 1105px) {
  .infoProduct {
    max-width: 500px;
    width: 100%;
    margin: 0 auto;
  }
}
</style>