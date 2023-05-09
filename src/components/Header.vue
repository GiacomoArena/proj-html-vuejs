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
  />

</div>


<div class="cart">
  <img src="../assets/icon/cart-icon.png" alt="cart">
  <button>LIVE STREAMING</button>

</div>
  

</section>

</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as*;
@import '../scss/partials/general' ;

section{
  //colore da togliere in futuro
  background-color: $my-blue;
  height: 105px;
  display: flex;
  align-items: center;
  justify-content: space-around;

  .link-menu{
    display: flex;
  }
  .cart{
    display: flex;
    align-items: center;
    img{
      width: 25px;
      height: 25px;
    }
    button{
      background-color: $my-lightgreen;
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
        border: 1px solid $my-lightgreen;
        padding: 5px;
        border-radius: 30px;
      }
    }
  }
}

</style>