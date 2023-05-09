<script >
import Header from './components/Header.vue';
import Jumbotron from './components/Jumbotron.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';
import {store} from "./data/store";


export default {
  name:'App',

  components:{
  Header,
  Footer,
  Jumbotron,
  Main
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

  <Jumbotron />

  <Main />

  <Footer />
</template>

<style lang="scss">
@import '../src/scss/Main.scss'  ;


</style>
