<template>
  <div id='questions'>
    <span id='title'>ответы на вопросы</span>
    <div id='list'>
      <Question question='что можно заказть в e-shop?' v-bind:answer='one'></Question>
      <Question question='как можно получить свой заказ?' v-bind:answer='two'></Question>
      <Question question='какими логистическими компаниями осуществлется доставка?' v-bind:answer='three'></Question>
      <Question question='сколько времени занимает доставка?' v-bind:answer='four'></Question>
      <Question question='есть ли в e-shop скидки?' v-bind:answer='five'></Question>
    </div>
  </div>
</template>

<script>
import Question from '@/components/Home/Question.vue'

export default {
  components: {
    Question
  },
  data() {
    return {
      one: 'E-SHOP специализируется на электронной технике. В нашем интернет-магазине Вы можете найти всё: от батареек до флагманских смарфонов. Также, по индивидуальному заказу, мы можем собрать Вам компьютер и доставить его прямо к квартире!',
      two: 'Мы предлагаем множество видов выдачи заказов: самовызов, доставка СДЭК, доставка Почтой России, доставка СБЕР Логистикой.',
      three: 'СДЭК, Почта России, СБЕР Логистика.',
      four: 'В зависимости от логичтической компании, но, как правило, не более пяти дней.',
      five: 'Конечно! Вы можете создать карту лояльности E-SHOP и получать скидку 5% на любой заказ, а также кэшбек в размере 1% от суммы покупки. при этом, если Вы впервые покупаете у нас, то сообщите об этом в комментариях к заказу и получите скидку 15%!'
    }
  }
}
</script>

<style scoped>
#questions {
  width: 60%; /* */
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}

#title {
  font-family: 'OswaldMedium';
  font-style: normal;
  font-weight: 500;
  font-size: 33px;
  line-height: 53px;
  text-align: center;
  letter-spacing: 0.02em;
  text-transform: uppercase;
  color: #000;
  margin-bottom: 2vh;
}

#list {
  width: 60vw;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

@media(max-width: 768px) {
  #questions {
    width: 80%;
    padding-top: 7vh;
  }

  #title {
    font-size: 26px;
    line-height: 42px;
  }

  #list {
    width: 100%;
  }
}
</style>