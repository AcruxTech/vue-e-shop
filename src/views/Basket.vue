<template>
  <div id='basket'>
    <Header></Header>
    <h1>Корзина</h1>
    <div id='products'>
      <ProductBasket v-for='product in products' :key='product.title' :product='product'></ProductBasket>
    </div>
    <div id='info'></div>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from '@/components/Shared/Header.vue'
import Footer from '@/components/Shared/Footer.vue'
import ProductBasket from '@/components/Basket/ProductBasket.vue'

export default {
  components: {
    Header,
    Footer,
    ProductBasket
  },
  data() {
    return {
      products: [
        {
          img: 'computer.png',
          title: 'Компьютер',
          text: 'text',
          cost: 10000
        },
        {
          img: 'laptop.jpg',
          title: 'Компьютер',
          text: 'text',
          cost: 10000
        },
        {
          img: 'phone.jpg',
          title: 'Компьютер',
          text: 'text',
          cost: 10000
        }
      ]
    }
  }
}
</script>

<style scoped>
#products {
  padding: 0 20%;
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}

h1 {
  margin-left: 20%;
  margin-top: 100px;
}
</style>
