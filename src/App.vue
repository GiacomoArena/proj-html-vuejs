<script >
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import {store} from "./data/store";


export default {
  name:'App',

  components:{
  Header,
  Footer,
},
data(){
      return{
        store
      }
    },
}


</script>


<template>

  <Header />

  


  <Footer />
</template>

<style lang="scss">
@import '../src/scss/Main.scss'  ;


</style>
