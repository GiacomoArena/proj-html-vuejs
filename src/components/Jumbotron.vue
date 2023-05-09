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
    <img class="controller" src="../assets/game-controler.png">
    <div class="side-container">
      <span>Game With Live Stearming</span>
      <h1>Future Of Esports</h1>
      <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium </p>
      <div class="buttons">
        <button>explore games <img src="../assets/svg/e-double-right-arrow.svg"></button>
      </div>
    </div>
    

  </section>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as*;

section{
  padding-top: 105px;
  position: relative;
  font-family: $primary-font;
  height: 900px;
  background-image: url(../assets/game-details-banner-bg.png);
  background-repeat: no-repeat;
  background-size:cover;
  .controller{
    position: absolute;
    top: 460px;
    left: 30px;
    z-index: 0;
  }
  .side-container{
    display: flex;
    flex-direction: column;
    justify-items: center;
    width: 540px;
    color: white;
    position: relative;
    z-index: 3;
    span{
      color: $my-lightgreen;
      font-weight: 600;
      font-size: 1.3rem;
    }
    h1{
      font-weight: 600;
      font-size: 4rem;
    }
    p{
      font-family: $secondary-font;
      font-size: 1.2rem;
    }
    .buttons{
      button{
      background-color: $my-green;
      border-radius: 25px;
      font-weight: 600;
      color: black;
      text-transform: uppercase;
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
      img{
        filter: brightness(0);
      }
    }
    }
  }
}
</style>