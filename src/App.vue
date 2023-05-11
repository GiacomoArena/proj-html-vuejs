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
        loading:true,
        scrollOff:true
      }
    },
    methods:{
      loadingPage(){
        setTimeout(() => {
          this.loading = false
        }, 2000);
      },
      scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });
    },
    scrolltrue(){
      this.scrollOff = true
    },
    scrollfalse(){
      this.scrollOff = false
    },
    },
    created(){
      this.loadingPage()
      this.scrolltrue()
    }
}


</script>


<template>
  <section class="preloader" 
  v-if="loading === true">
  <img src="./assets/preloader.gif" alt="preloader">
  </section>


  <section v-else class="all-component">

    <Header />
  
    <Jumbotron 
    @scrolltrue="scrolltrue()"
    />
  
    <Main 
    @scrollfalse="scrollfalse()"
    />
  
    <Footer />

    <button :class="{'scroll-off' : scrollOff === true}"
    @click="scrollToTop()" 
    class="scroll-top"
    >
      <i class="fa-solid fa-angles-up"></i>
    </button>
  </section>
  
</template>

<style lang="scss">
@use './scss/partials/variables' as *;
@import '../src/scss/Main.scss'  ;

.preloader{
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background-color: #1B253B;
}
.all-component{
  position: relative;
  .scroll-off{
    bottom: -100px !important;
    opacity: 0 !important;
  }
  .scroll-top{
    padding: 10px 15px;
    border: none;
    color: $my-white;
    background-color: $my-lightgreen;
    border-radius: 10px;
    position: fixed;
    right: 30px;
    bottom: 40px;
    z-index: 99999;
    transition: all 1s;
    opacity: 1
    ;
  }
}
</style>
