  <script>
  

  export default {
    name:'LatestNews',
    data(){
      return{
        cards:[
          {
            description:'Top 5 Most Important Aspects Of Your Game ',
            src:'/public/blog-item-2.png'
          },
          {
            description:'The Rise Of Fantasy Sports And Online Games',
            src:'/public/blog-item-3.png'
          },
          {
            description:'Benefits Of Gaming - PC And Video Games',
            src:'/public/blog-item-4.png'
          },
        ]
      }
    }
  }
  </script>


<template>
  <section>
    <div class="text-section">
      <span>Latest News</span>
      <h1>
        Stay Updated With Our Latest News Articles
      </h1>
      <p>
        libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Cras ultricies ligula sed magna dictum porta.
      </p>
  </div>

  <div class="cards-containers">
    <div class="big-card">
      <img class="player" src="../../assets/blog-item-1.png" alt="user">
      <div class="text">
          <span>
            <img src="../../assets/icon/clock.png" >
            10 Min
            <img src="../../assets/icon/eye.png">
            240
            <img src="../../assets/icon/calendar.png">
            Apr 11,2022
          </span>
          <p>
            Secrets To An Amazing Role Playing Game
          </p>
        </div>
    </div>
    <div class="side-container">

      <div class="cards d-flex" v-for="(card,i) in cards" :key="i">
        <img class="player" :src="card.src" alt="user">
        <div class="text-side">
          
          <span>
            <img src="../../assets/icon/clock.png" >
            10 Min
            <img src="../../assets/icon/eye.png">
            240
            <img src="../../assets/icon/calendar.png">
            Apr 11,2022
          </span>
          <p>
            {{card.description}}
          </p>
        </div>

      </div>

    </div>
  </div>

  </section>
</template>


<style lang="scss" scoped>
@use '../../scss/partials/variables' as*;
  section{
    padding-bottom: 300px;
    font-family: $primary-font;
    background-color: black;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    .text-section{
      max-width: 700px;
      span{
        color: $my-lightgreen;
        font-size: 1.3rem;
        font-weight: 600;
      }
      h1{
        color: white;
        font-size: 3.2rem;
        font-weight: 600;
      }
      p{
        font-family: $secondary-font;
        color: $my-white;
      }
    }
    .cards-containers{
      margin-top:20px;
      display: flex;
      .big-card{
        background-color: $my-blue;
        border-radius: 20px;
        max-width: 640px;
        min-width: 300px;
        height: 550px;
        img.player{
          cursor: pointer;
          width: 100%;
          object-fit: cover;
        }
        .text{
          text-align: left;
          margin-top: 20px;
          margin-left: 20px;
          img{
            margin-left: 20px;
          }
          span{
            color: $my-lightgreen;
          }
          p{
            cursor: pointer;
            padding: 10px;
            margin-top: 15px;
            font-size: 1.9rem;
            color: white;
            font-weight: 600;
          }
        }
      }
      .cards{
        margin-left: 20px;
        margin-bottom: 20px;
        background-color: $my-blue;
        display: flex;
        align-items: center;
        border-radius: 20px;
        width: 600px;
        
        img.player{
          cursor: pointer;
          border-radius: 20px;
          object-fit: cover;
        }
        .text-side{
          img{
            margin-left: 20px;
          }
          span{
            color: $my-lightgreen;
          }
          p{
            cursor: pointer;
            padding: 10px;
            margin-top: 15px;
            font-size: 1.5rem;
            color: white;
            font-weight: 600;
          }
        }
      }
    }

  }
</style>