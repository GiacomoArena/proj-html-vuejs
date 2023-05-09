  <script>
  

  export default {
    name:'TrendingBattle',
    data(){
      return{
        
      }
    }
  }
  </script>


<template>
  <section>
    <div class="text">
      <span>Trending Battle</span>
      <h1>Keep Eyes & Manage Upcoming Battle</h1>
      <p>
        libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Cras ultricies ligula sed magna dictum porta.
      </p>
    </div>
  </section>
  <div class="card-container">
    <div class="row justify justify-content-center">
<!-- CARD1 -->
      <div class="col-5 card  me-3 d-flex flex-column">
        <div class="card-items">
          <img src="../../assets/game-img-1.png" alt="team">
          <img class="vs" src="../../assets/verus-icon.png" alt="team">
          <img src="../../assets/game-img-2.png" alt="team">
        </div>
        
        <span>
          <h3>Call Of Deauty</h3>
          <p>December 25, 2022 4:00 PM</p>
        </span>

        <div class="social">
          
            <img src="../../assets/icon/youtube-icon.png" alt="">
            <a href="#">Youtube</a>
          
            <img src="../../assets/icon/twitch-icon.png" alt="">
            <a href="#">Twitch</a>
          
        </div>
      </div>
<!-- ///---CARD 1---///-->
<!-- CARD 2-->
      <div class="col-5 card  me-3 d-flex flex-column">
        <div class="card-items">
          <img src="../../assets/game-img-3.png" alt="team">
          <img class="vs" src="../../assets/verus-icon.png" alt="team">
          <img src="../../assets/game-img-4.png" alt="team">
        </div>
        
        <span>
          <h3>Legendary Battles</h3>
          <p>December 25, 2022 4:00 PM</p>
        </span>

        <div class="social">
          
            <img src="../../assets/icon/youtube-icon.png" alt="">
            <a href="#">Youtube</a>
          
            <img src="../../assets/icon/twitch-icon.png" alt="">
            <a href="#">Twitch</a>
          
        </div>
      </div>
<!-- ///---CARD 2---///-->
<!-- CARD 3-->
      <div class="col-5 card  me-3 mt-4 d-flex flex-column">
        <div class="card-items">
          <img src="../../assets/game-img-5.png" alt="team">
          <img class="vs" src="../../assets/verus-icon.png" alt="team">
          <img src="../../assets/game-img-6.png" alt="team">
        </div>
        
        <span>
          <h3>Nay Corral Gundown</h3>
          <p>December 25, 2022 4:00 PM</p>
        </span>

        <div class="social">
          
            <img src="../../assets/icon/youtube-icon.png" alt="">
            <a href="#">Youtube</a>
          
            <img src="../../assets/icon/twitch-icon.png" alt="">
            <a href="#">Twitch</a>
          
        </div>
      </div>
<!-- ///---CARD3 ---///-->
<!-- CARD 4-->
      <div class="col-5 card  me-3 mt-4  d-flex flex-column">
        <div class="card-items">
          <img src="../../assets/game-img-7.png" alt="team">
          <img class="vs" src="../../assets/verus-icon.png" alt="team">
          <img src="../../assets/game-img-8.png" alt="team">
        </div>
        
        <span>
          <h3>League Of Legends</h3>
          <p>December 25, 2022 4:00 PM</p>
        </span>

        <div class="social">
          
            <img src="../../assets/icon/youtube-icon.png" alt="">
            <a href="#">Youtube</a>
          
            <img src="../../assets/icon/twitch-icon.png" alt="">
            <a href="#">Twitch</a>
          
        </div>
      </div>
<!-- ///---CARD 4---///-->
    </div>
    <div class="button">
    <button>
      view all match
      <img src="../../assets/svg/e-double-right-arrow.svg" >
    </button>
  </div>
  
  </div>
</template>


<style lang="scss" scoped>
@use '../../scss/partials/variables' as*;
  section{
    font-family: $primary-font;
    display: flex;
    justify-content: center;
    padding-top: 100px ;
    background-color: #222833;
    color: white;
    .text{
      max-width: 700px;
      text-align: center;
      span{
        color: $my-lightgreen;
        font-size: 1.2rem;
        font-weight: 600;
      }
      h1{
        font-size: 3.2rem;
        font-weight: 600;
      }
      p{
        font-family: $secondary-font;
        color: $my-white;
      }
    }
  }
  .card-container{
    padding-top: 30px;
    padding-bottom: 200px;
    background-color: #222833;
    .button{
      button{
          font-family: $secondary-font;
          background-color: $my-green;
          border-radius: 25px;
          font-weight: 600;
          color: black;
          text-transform: uppercase;
          padding: 10px;
          position: relative;
          display: inline-flex;
          align-items: center;
          justify-content: center;
          margin: 5px;
          transition: 0.3s all;
          border: none;
          bottom: -80px;
          left: 50%;
          transform: translateX(-50%);
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
          width: 15px;
          filter: brightness(0);
          margin-left: 5px;
        }
      }
    }
    .card{
      max-width: 630px;
      min-width: 300px;
      background-color: #283449;
      border-color: #3E5172;
      
      .card-items{
        padding: 30px;
        display: flex;
        justify-content: space-between;
        img{
          width: 150px;
        }
        .vs{
          width: 60px;
          height: 120px;
        }
      }
      span{
          font-family: $primary-font;
          padding: 20px 0;
          width: 100%;
          background-color: $my-blue;
          text-align: center;
          h3{
            font-size: 1.4rem;
            font-weight: 600;
            color: white;
          }
          p{
            font-size: .9rem;
            color: $my-lightgreen;
          }
        }
    }
  }
  .social{
    background-color: #283449;
    width: 100%;
    padding: 40px 0;
    display: flex;
    justify-content: center;
    align-items: center;
    a{
      text-decoration: none;
      color: $my-white;
      margin-right: 30px;
    }
  }
</style>