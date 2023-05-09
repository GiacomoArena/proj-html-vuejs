  <script>
  

  export default {
    name:'Jumbotron',
    data(){
      return{
        
      }
    }
  }
  </script>


<template>
  <section>
    <div class="side-container">
      <img class="controller" src="../assets/game-controler.png">
      <span>Game With Live Stearming</span>
      <h1>Future Of Esports</h1>
      <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium </p>
    </div>
    

  </section>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as*;

section{
  padding-top: 105px;
  height: 900px;
  background-image: url(../assets/game-details-banner-bg.png);
  background-repeat: no-repeat;
  background-size:cover;
  .side-container{
    width: 540px;
    color: white;
    position: relative;
    z-index: 3;
    .controller{
      position: absolute;
      z-index: 0;
    }
  }
}
</style>