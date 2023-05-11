  <script>
  import {store} from "../data/store";
  import HeaderLinks from '../components/partials/HeaderLinks.vue'
  import {products} from '../data/db'

  export default {
    name:'Headers',
    components:{
      HeaderLinks
    },
    data(){
      return{
        store,
        products,
        cartFlag:false
      }
    },
    methods:{
      changeCartFlag(){
        this.cartFlag = !this.cartFlag
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


<div class="cart" @click="changeCartFlag()">
  <img src="../assets/icon/cart-icon.png" alt="cart">
  <button>LIVE STREAMING</button>
  <span class="element-num">
    03
  </span>
  <div class="cart-element" :class="{'click-cart-element' : cartFlag === true}">
    <span class=" d-flex justify-content-between">
    <h6>Cart</h6>
      03
    </span>
    <div class="product d-flex"
    v-for="(product, i) in products" :key="i">

      <img :src="product.src" alt="shop-img">
      <span>
        <h5>{{product.name}}</h5>
        $380.00
        <span class="discount">
          $410.00
        </span>
      </span>
    </div>
    <button class="checkout">CHECKOUT</button>
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
    .click-cart-element{
      right: 190px;
      top: 85px !important;
      opacity: 1 !important;
      pointer-events: auto !important;
    }
    .cart-element{
      pointer-events: none;
      border-radius: 10px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-content: center;
      position: absolute;
      width: 300px;
      padding: 10px;
      padding-bottom: 100px;
      background-color: $my-blue;
      right: 190px;
      top: 385px;
      opacity: 0;
      transition: all 0.6s;
      span{
        padding: 10px 0;
        align-items: center;
        color: $my-white;
        font-weight: 600;
        h6{
          font-weight: 600;
          color: white;
          font-family: $primary-font;
          font-size: 1.7rem;
        }
      }

      .checkout{
        position: absolute;
        bottom: 10px;
        left: 50%;
        transform: translateX(-50%);
        width: 120px;
      }
        
      .product{
        border-radius: 10px;
        justify-content: center;
        align-items: center;
        width: 100%;
        padding: 5px;
        border: 1px solid #3E5172;
        img{
          margin: 0;
          margin-left: 5px;
          width: 80px;
          height: 80px;
        }
        span{
          margin-left: 10px;
          color: $my-lightgreen;
        }
        h5{
          color: $my-white;
          font-family: $primary-font;
          font-weight: 600;
        }
        .discount{
          color: $my-white;
          text-decoration: line-through;
        }
      }
    }
    .element-num{
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