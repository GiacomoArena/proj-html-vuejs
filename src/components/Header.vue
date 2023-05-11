  <script>
  import {store} from "../data/store";
  import HeaderLinks from '../components/partials/HeaderLinks.vue'

  export default {
    name:'Headers',
    components:{
      HeaderLinks
    },
    data(){
      return{
        store
      }
    }
  }
  </script>


<template>

<section>


  <img src="../assets/logo.png" alt="logo">


<div class="link-menu">
  <HeaderLinks 
  v-for="(link,i) in store.haderLinks"
  :key="i"
  :link="link.text"
  :i="i"
  />

</div>


<div class="cart">
  <img src="../assets/icon/cart-icon.png" alt="cart">
  <button>LIVE STREAMING</button>
  <span class="element-num">
    03
  </span>
  <div class="cart-element">
    <span class="d-flex">
      <h6>Cart</h6>
      03
    </span>
    <div class="product d-flex">
      <img src="../assets/shop-image-3.png" alt="shop-img">
      <span>
        <h5>Havit RGB Headphone</h5>
      </span>
    </div>
  </div>
</div>
  

</section>

</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as*;
@import '../scss/partials/general' ;

section{
  position: fixed;
  z-index: 9999;
  width: 100%;
  font-family: $primary-font;
  background-color: $my-darkblue;
  height: 105px;
  display: flex;
  align-items: center;
  justify-content: space-around;
  img{
    cursor: pointer;
  }
  .link-menu{
    display: flex;
    text-transform: capitalize;
    font-weight: 600;
  }
  .cart{
    font-family: $secondary-font;
    position: relative;
    display: flex;
    align-items: center;
    cursor: pointer;
    .cart-element{
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      position: absolute;
      width: 300px;
      height: 100%;
      padding: 15px;
      background-color: $my-blue;
      right: 190px;
      top: 85px;
    }
    span.element-num{
      text-align: center;
      width: 20px;
      position: absolute;
      background-color: $my-green;
      font-size: 13px;
      font-weight: 600;
      right: 178px;
      top: 8px;
      border-radius: 50%;
    }
    img{
      margin: 0 15px;
      width: 25px;
      height: 25px;
      cursor: pointer;
    }
    button{
      background-color: $my-green;
      border-radius: 25px;
      font-weight: 600;
      color: black;
      padding: 10px 20px;
      position: relative;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      margin: 5px;
      transition: 0.3s all;
      border: none;
      &::after{
        position: absolute;
        content: "";
        width: 108%;
        height: 120%;
        border: 1px solid $my-green;
        padding: 5px;
        border-radius: 30px;
      }
      &:hover::after{
        border-color: $my-lightgreen;
      }
      &:hover{
        background-color: $my-lightgreen;
      }
    }
  }
}

</style>