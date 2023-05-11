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
        store,
        loading:true
      }
    },
    methods:{
      loadingPage(){
        setTimeout(() => {
          this.loading = false
        }, 2000);
      }
    },
    created(){
      this.loadingPage()
    }
}


</script>


<template>
  <section class="preloader" 
  v-if="loading === true">
  <img src="./assets/preloader.gif" alt="preloader">
  </section>


  <section v-else>
    <Header />
  
    <Jumbotron />
  
    <Main />
  
    <Footer />
  </section>
  
</template>

<style lang="scss">
@import '../src/scss/Main.scss'  ;
.preloader{
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background-color: #1B253B;
}

</style>
