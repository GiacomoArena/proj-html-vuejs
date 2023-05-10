  <script>
  

  export default {
    name:'Discount',
    data(){
      return{
        
      }
    }
  }
  </script>


<template>
  
  <section>
    <div class="discount-bg">
      <h3>Make Offer</h3>
      <h1>Get 70% Offer Discount</h1>
      <button>Get Offers</button>
    </div>
  </section>
</template>


<style lang="scss" scoped>
@use '../../scss/partials/variables' as*;
  section{
    background-color: black;
    padding-bottom: 100px;
    
    .discount-bg{
      color: white;
      font-family: $primary-font;
      border-radius: 15px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      width: 80%;
      margin: 0 auto;
      min-height: 400px;
      background-image: url(../../assets/banner-item-bg.png);
      background-size: cover;
      h3{
        font-weight: 600;
        font-size: 1.4rem;
      }
      h1{
        font-weight: 600;
        font-size: 3rem;
      }
      button{
        color: white;
        font-family: $secondary-font;
        background-color: #1A8F3D;
        border: none;
        padding: 10px 30px;
        border-radius: 25px;
        transition: all 1.5s;
        &:hover{
          background-color: $my-lightgreen;
        }
      }
    }
  }
</style>