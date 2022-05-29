<template>
  <div id='product'>
    <div id='image'>
      <img :src="require(`../../assets/images/${product.img}`)" alt='product'/>
    </div>
    <div id='info'>
      <div id='desc'>
        <span id='title'>{{product.title}}</span>
        <span id='text'>{{product.text}}</span>
      </div>
      <div id='order'>
        <span id='cost'>{{product.cost}}&#8381;</span>
        <button type='button'><img src='@/assets/icons/basket.svg' alt='basket'></button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    product: Object
  }
}
</script>

<style scoped>
#product {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: space-between;
  box-shadow: 0px 0px 25px 5px rgba(34, 60, 80, 0.2);
  border-radius: 15px;
  height: 20vh;
  width: 100%;
  margin: 2% 0;
}

#image {
  width: 35%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

#image > img { height: 90%; }

#info {
  height: 100%;
  width: 65%;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: flex-start;
}

#title, #cost {
  font-family: 'OswaldMedium';
  font-style: normal;
  font-weight: 500;
  font-size: 36px;
  text-align: center;
  text-transform: uppercase;
}

#cost { font-size: 30px; }

#text {
  font-family: 'OpenSansRegular';
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  color: #999;
}

#desc {
  height: 100%;
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: flex-start;
}

#order {
  height: 100%;
  width: 50%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

button {
	width: 5vh;
  height: 5vh;
	justify-content: center;
	color: #fff;
	background: #2C63B5;
	font-size: 1em;
	font-weight: bold;
	outline: none;
	border: none;
	border-radius: 50%;
	transition: .2s ease-in;
	cursor: pointer;
  transition: .5s;

  display: flex;
  align-items: center;
  justify-content: center;
}

button > img {
  width: 80%;
}
</style>