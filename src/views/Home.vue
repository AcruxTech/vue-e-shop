<template>
  <div id='home'>
    <Header></Header>
    <Carusel></Carusel>
    <OurServices></OurServices>
    <Questions></Questions>
    <Contacts></Contacts>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from '@/components/Shared/Header.vue'
import Carusel from '@/components/Home/Carusel.vue'
import Footer from '@/components/Shared/Footer.vue'
import OurServices from '@/components/Home/OurServices.vue'
import Questions from '@/components/Home/Questions.vue'
import Contacts from '@/components/Home/Contacts.vue'

export default {
  components: {
    Header,
    Carusel,
    OurServices,
    Questions,
    Contacts,
    Footer
  }
}
</script>

<style scoped>
#home {
  width: 100%;
  padding-top: 100px;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
