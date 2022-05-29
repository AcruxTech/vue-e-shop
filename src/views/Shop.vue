<template>
  <div id='shop'>
    <Header></Header>
    <div id='categories'>
      <span class='category'>Все товары</span>
      <span class='category'>Компьютеры</span>
      <span class='category'>Ноутбуки</span>
      <span class='category'>Смартфоны</span>
      <span class='category'>Аксессуары</span>
    </div>
    <h1>Найдено 5 товаров:</h1>
    <div id='products'>
      <Product v-for='product in products' :key='product.title' :product='product'></Product>
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from '@/components/Shared/Header.vue'
import Footer from '@/components/Shared/Footer.vue'
import Product from '@/components/Shop/Product.vue'

export default {
  components: {
    Header,
    Footer,
    Product
  },
  data() {
    return {
      products: [
        {
          img: 'computer.png',
          title: 'Компьютер',
          text: 'Intel Core i5, GTX1660, 16Gb Ram',
          cost: 10000
        },
        {
          img: 'phone.jpg',
          title: 'IPHONE 13',
          text: '128Gb, камера 50мп',
          cost: 10000
        },
        {
          img: 'computer.png',
          title: 'Компьютер',
          text: 'Intel Core i5, GTX1660, 16Gb Ram',
          cost: 10000
        },
        {
          img: 'computer.png',
          title: 'Компьютер',
          text: 'Intel Core i5, GTX1660, 16Gb Ram',
          cost: 10000
        },
        {
          img: 'computer.png',
          title: 'Компьютер',
          text: 'Intel Core i5, GTX1660, 16Gb Ram',
          cost: 10000
        },
        {
          img: 'computer.png',
          title: 'Компьютер',
          text: 'Intel Core i5, GTX1660, 16Gb Ram',
          cost: 10000
        },
        {
          img: 'computer.png',
          title: 'Компьютер',
          text: 'Intel Core i5, GTX1660, 16Gb Ram',
          cost: 10000
        }
      ]
    }
  }
}
</script>

<style scoped>
#shop {
  width: 100%;
  padding-top: 100px;
}

#products {
  padding: 0 20%;
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;
  flex-wrap: wrap;
}

h1 {
  margin-left: 20%;
}

#categories {
  padding: 2% 20%;
}

.category {
  margin-right: 30px;
  padding: 10px;
  border-radius: 15px / 50%;
  background-color: #eee;
  font-family: 'OpenSansRegular';
  font-style: normal;
  font-weight: 400;
  font-size: 24px;
  color: #777;
  box-shadow: 0px 0px 5px 3px rgba(34, 60, 80, 0.2);
}
</style>
