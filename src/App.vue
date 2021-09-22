<template>
  <div id="app">
    <Header/>
    <main>
      <Banner/>
      <ChooseComics/>    
    </main>
    <Footer/>
    </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Banner from '@/components/Banner.vue'
import ChooseComics from '@/components/ChooseComics.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Banner,
    ChooseComics,
    Footer,
  }
}
</script>

<style lang="scss" scoped>
@import "style/generals";
</style>
