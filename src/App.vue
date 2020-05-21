<template>
  <div id="app">
    <h1>eShop</h1>
    <Header />

    
    <main>
      <GoodsList
        v-bind:goods="goods"
      />

    </main>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Basket from '@/components/Basket.vue'
import GoodsList from '@/components/GoodsList.vue'

export default {
  name: 'App',
  data() {
    return{
      goods: [
  {"id_product": 123, "product_name": "Ноутбук","price": 45600},
  {"id_product": 456, "product_name": "Мышка", "price": 1000}
      ]
    }
  },
  //  mounted(){
  //       fetch('https://raw.githubusercontent.com/GeekBrainsTutorial/online-store-api/master/responses/catalogData.json')
  //       .then(response => response.json())
  //       .then(json => {
  //       this.products = json
  //   })
  //  },
   components: {
    Header,
    Basket,
    GoodsList
  },
}



</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
