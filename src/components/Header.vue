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

<div class="logo">
  <img src="../assets/logo.png" alt="logo">
</div>

<div class="link-menu">
  <HeaderLinks 
  v-for="(link,i) in store.haderLinks"
  :key="i"
  :link="link.text"
  />
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

  .logo{
    width: 100%;
  }
}

</style>