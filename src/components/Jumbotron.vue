  <script>
  

  export default {
    name:'Jumbotron',
    data(){
      return{
        
      }
    }
  }
  </script>


<template >
  <!-- I create a $emit that will change the value of a flag for me that is used to make the button that sends you to the top page visible or not -->
  <section  @mouseover="$emit('scrolltrue')">
    <img class="controller" src="../assets/game-controler.png">
    <div class="side-container">
      <span>Game With Live Stearming</span>
      <h1>Future Of Esports</h1>
      <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium </p>
      <div class="buttons">
        <button>explore games <img src="../assets/svg/e-double-right-arrow.svg"></button>

        <a href="https://www.youtube.com/watch?v=Djz8Nc0Qxwk" >
          <img class="play" src="../assets/icon/play-icon.png" alt="play">
        </a>

      </div>

    </div>

    <div class="big-logo">
      <a href="#">
        <img src="../assets/index-banner-illus.png" alt="logo">
      </a>
    </div>
    

  </section>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as*;

section{
  padding-top: 105px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-around;
  font-family: $primary-font;
  height: 900px;
  background-image: url(../assets/game-details-banner-bg.png);
  background-repeat: no-repeat;
  background-size:cover;
  .controller{
    position: absolute;
    top: 480px;
    left: 30px;
    z-index: 0;
  }
  .side-container{
    margin-left: 50px;
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
        margin-left: 5px;
      }
    }
    a{
      width: 50px;
      height: 50px;
      position: relative;
      margin-left: 40px;
      padding: 10px;
      background-color: $my-white;
      border-radius: 50%;
      cursor: pointer;
      &::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        border: 1px solid $my-green;
        border-radius: 50%;
        transform: scale(1.1);
        transition: transform 0.2s ease-out;
        z-index: -1;
        &{
          transform: scale(0.9);
          animation: pulse 1s infinite alternate ease-in-out;
        }
        @keyframes pulse {
          0% {
            transform: scale(1.6);
          }
          100% {
            transform: scale(1.3);
          }
        }
    }
      }
        }
    }
  .big-logo{
    img{
      width: 100%;
    }
  }
}
</style>