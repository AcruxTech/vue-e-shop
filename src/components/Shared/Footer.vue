<template>
  <div id='footer'>
    <span class='text'>&#169; 2022 E-SHOP</span>
    <span class='text'>powered by AcruxTech</span>
  </div>
</template>

<style scoped>
  #footer {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    width: 100%; /* */
    height: 100px;
    margin-top: 5vh;
    background-color: #404149;
    padding: 0 20vw;
  }
  .text {
    font-family: 'OpenSansRegular';
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 22px;
    color: #FFFFFF;
  }
  @media (max-width:768px) {
    #footer {
      height: 80px;
      padding: 0 10vw;
      margin-top: 7vh;
    }
    .text {
      font-size: 15px;
    }
  }
</style>