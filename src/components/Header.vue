<template>
  <div class="header">
    <img src="@/assets/images/Logo.svg" alt="my-logo" />
    <div class="blockImages">
      <img src="@/assets/images/Person.svg" alt="">
      <img src="@/assets/images/Favorite.svg" alt="">
      <img src="@/assets/images/Bag.svg" alt="">
    </div>
  </div>
</template>

<script lang="ts">

export default {
  name: 'Header'

}
</script>

<style scoped>
.header {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  height: 40px;
  width: 100%;
}

.blockImages {
  flex-grow: 1;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-end;
  gap: 25px;
}
</style>