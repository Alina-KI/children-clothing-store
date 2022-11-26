<template>
  <Header />
  <Footer/>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'

@Options({
  components: {
    Footer,
    Header
  }
})
export default class App extends Vue {
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  max-width: 1390px;
  width: 100%;
  height: 100vh;
  margin: 0 auto;
}
</style>
