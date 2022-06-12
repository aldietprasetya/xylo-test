<template>
  <div id="app">
    <Header></Header>
    <HeaderDesktop></HeaderDesktop>

    <router-view/>

    <Footer></Footer>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import HeaderDesktop from './components/HeaderDesktop.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    HeaderDesktop,
    Footer,
  }
}
</script>

<style lang="scss">
// MyCarrousel.vue
@import 'slick-carousel/slick/slick.css';
@import './assets/scss/style';
</style>
