<template>
  <div id='carusel'>
    <div id='arrows'>
      <img src='@/assets/icons/arrow.svg' id='left' @click='change(-1)'/>
      <img src='@/assets/icons/arrow.svg' id='rigth' @click='change(1)'/>
    </div>
    <carusel-slide v-for='slide in slides' :key='slide.title' :slide='slide' 
      :isShow='slideNumber == slides.indexOf(slide) ? true : false'></carusel-slide>
  </div>  
</template>

<script>
import CaruselSlide from './CaruselSlide.vue';

export default {
  components: {
    CaruselSlide
  },
  data() {
    return {
      counter: 0,
      slideNumber: 0,
      slides: [
        {
          title: 'Ноутбуки',
          text: 'От моделей для офиса до игровых ультрабуков',
          img: 'laptop.jpg'
        },
        {
          title: 'Смартфоны',
          text: 'Здесь Вы найдете телефон на любой вкус',
          img: 'phone.jpg'
        },
        {
          title: 'Персональные компьютеры',
          text: 'Окунитесь в мир игр с последними моделями игровых ПК!',
          img: 'computer.png'
        }
      ]
    }
  },
  methods: {
    change(value) {
      if (this.slideNumber + value >= this.slides.length) this.slideNumber = 0;
      else if (this.slideNumber + value <= -1) this.slideNumber = this.slides.length-1;
      else this.slideNumber += value;
      console.log(this.slideNumber);
    }
  }
}
</script>

<style scoped>
#carusel {
  width: 100%;
  height: 70vh;
  border-bottom: 5px solid #eee;
  display: flex;
  align-items: center;
  justify-content: center;
}

#arrows {
  position: absolute;
  top: 100px;
  right: 20vw;
  padding: 1% 0;
  width: 7%;
  height: auto;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

img { width: 35%; }

#left { transform: scale(-1, 1); }
</style>