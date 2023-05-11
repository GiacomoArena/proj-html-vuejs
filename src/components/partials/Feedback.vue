  <script>
  

  export default {
    name:'Feedback',
    data(){
      return{
        cards:[
          {
            name:'Merle Fisher',
            country:'United States',
            src:'/public/testimonials-image-1.png'
          },
          {
            name:'Garry Francis',
            country:'Kiribati',
            src:`/public/testimonials-image-2.png`
          },
          {
            name:'Kim Ramos',
            country:'Serbia',
            src:'/public/testimonials-image-3.png'
          },
        ]
      }
    }
  }
  </script>


<template>
  <section>

    <div class="text-section">
      <span>Futio Feedback</span>
      <h1>What Our Gamers Say</h1>
      <p>
        libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Cras ultricies ligula sed magna dictum porta.
      </p>
  </div>
<div class="card-container d-flex">
<!-- I dynamically generate cards with v-for -->
  <div class="card" v-for="(card,i) in cards " :key="i">
    <div class="text">
      <span>
        <i class="fa-solid fa-star"></i>
        <i class="fa-solid fa-star"></i>
        <i class="fa-solid fa-star"></i>
        <i class="fa-solid fa-star"></i>
        <i class="fa-solid fa-star"></i>
      </span>
      <p>
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor"
      </p>

    </div>
    <div class="testimonial">
      <img :src="card.src" :alt="card.name">
      <span>
        <h6>{{card.name}}</h6>
        {{card.country}}
      </span>
    </div>
  </div>
</div>
  
  </section>
</template>


<style lang="scss" scoped>
@use '../../scss/partials/variables' as*;
  section{
    font-family: $primary-font;
    padding: 100px 0;
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
        font-size: 1.2rem;
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
      .card{
        margin: 10px;
        padding: 20px;
        background-color: $my-blue;
        color: white;
        text-align: start;
        max-width: 350px;
        display: flex;
        border-radius: 25px;
        justify-content: flex-start;
        .text{
          margin-left: 25px;
          font-family: $secondary-font;
          font-size: 1.1rem;
          font-weight: 500;
          i{
            color: #FFBA00;
          }
        }
        .testimonial{
          width: 100%;
          height: 40px;
          display: flex;
          align-items: center;
          img{
            object-fit: cover;
            
          }
          margin-left: 25px;
          display: flex;
          span{
            font-family: $secondary-font;
            color: $my-lightgreen;
            margin-left: 15px;
            h6{
              font-family: $primary-font;
              color: white;
              font-size: 1.1rem;
              font-weight: 600;
            }
          }
        }
      }
    }
</style>