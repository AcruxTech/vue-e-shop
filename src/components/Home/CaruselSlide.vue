<template>
  <div id='caruselSlide' v-bind:class='{show: !isShow}'>
    <img :src="require(`../../assets/images/${slide.img}`)" alt="alt">
    <div id='info'>
      <span id='title'>{{slide.title}}</span>
      <span id='text'>{{slide.text}}</span>
      <button type='button' @click='$router.push("shop")'>Купить</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    slide: Object,
    isShow: Boolean
  }
}
</script>

<style scoped>
#caruselSlide {
  width: 60%;
  height: 80%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: .5s;
}

#caruselSlide.show { display: none; }

img { height: 75%; }

#info {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  height: 40%;
}

#title {
  font-family: 'OswaldMedium';
  font-style: normal;
  font-weight: 500;
  font-size: 50px;
  text-align: center;
  text-transform: uppercase;
}

#text {
  font-family: 'OpenSansRegular';
  font-style: normal;
  font-weight: 400;
  font-size: 24px;
  color: #999;
}

button {
	width: 35%;
  height: 4.5vh;
	justify-content: center;
	color: #fff;
	background: #2C63B5;
	font-size: 1em;
	font-weight: bold;
	outline: none;
	border: none;
	border-radius: 15px;
	transition: .2s ease-in;
	cursor: pointer;
  transition: .5s;
}

button:hover {
  background: #387ce3;
}
</style>