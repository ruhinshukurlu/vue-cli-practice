<template>
  <div id="app">
    <Header/>

    <div class="container mt-5 mb-5">
      <div class="row">
        <app-child  v-for="unit in manifest" :item="unit.item" :url="unit.url" :desc='unit.desc'></app-child>
      </div>
    </div>

    <Footer/>
  </div>
</template>

<script>

  import AppChild from '@/components/AppChild.vue'
  import Header from './components/Header.vue'
  import Footer from './components/Footer.vue'

  export default {
    components : {
      AppChild,
      Header,
      Footer
    },
    data() {
      return {
        manifest: [
          {
            item: "backpack",
            url:"https://media.gq-magazine.co.uk/photos/5f575108020908336ccd4d82/master/w_1000,c_limit/20200907-tshirt-05.jpg",
            desc : 'Some quick example text to build on the card title and make up the bulk of the cards content.'
          },
          {
            item: "tshirt",
            url: "https://imgs.michaels.com/MAM/assets/1/726D45CA1C364650A39CD1B336F03305/img/91F89859AE004153A24E7852F8666F0F/10093625_r.jpg?fit=inside|1024:1024",
            desc : 'Some quick example text to build on the card title and make up the bulk of the cards content.'
          },
          {
            item: "sweatshirt",
            url: "https://www.openbsd.org/images/tshirt-53-coralfever.jpg",
            desc : 'Some quick example text to build on the card title and make up the bulk of the cards content.'
          },
        ],
      };
    },
  };
</script>

<style lang="scss">
</style>
