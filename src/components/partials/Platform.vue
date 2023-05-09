  <script>
  

  export default {
    name:'Platform',
    data(){
      return{
        
      }
    }
  }
  </script>


<template>
  <section>
    
    <img src="../../assets/features-illus.png" alt="img">

    <div class="info">
      <p>The Ultimate Competitive Gaming Platfrom</p>
      <h1>Make Your Mark On The Battle Field</h1>
      <span>
        libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Cras ultricies ligula sed magna dictum porta.
      </span>
      <div class="features">

        <div class="live-streaming d-flex mt-2">
          <img src="../../assets/icon/features-icon-1.png" alt="icon">
          <span>
            <h3>Live Streaming</h3>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labor.
            </p>
          </span>
        </div>

        <div class="great-tournament d-flex mt-2">
          <img src="../../assets/icon/features-icon-2.png" alt="icon">
          <span>
            <h3>Great Tournament</h3>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labor.
            </p>
          </span>
        </div>

        <div class="gaming-news d-flex mt-2">
          <img src="../../assets/icon/features-icon-3.png" alt="icon">
          <span>
            <h3>Gaming News</h3>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labor.
            </p>
          </span>
        </div>

      </div>
    </div>
  </section>
</template>


<style lang="scss" scoped>
@use '../../scss/partials/variables' as*;
  section{
    height: 900px;
    background-color: black;
    display: flex;
    justify-content: space-around;
    align-items: center;
    img{
      width: 50%;
      object-fit: contain;
    }
    .info{
      font-family: $primary-font;
      width: 40%;
      color: white;
      p{
        color: $my-lightgreen;
        font-size: 1.2rem;
        font-weight: 600;
      }
      h1{
        font-size: 3.2rem;
        font-weight: 600;
      }
      span{
        font-family: $secondary-font;
      }
      .features{
        margin-top: 20px;
        display: flex;
        flex-direction: column;
        img{
          width: 80px;
          margin-right: 25px;
        }
        h3{
          font-family: $primary-font;
          font-size: 1.5rem;
          font-weight: 600;
        }
        span{
          display: flex;
          flex-direction: column;
        }
        p{
          color: $my-white;
          font-family: $secondary-font;
          font-weight: 400;
          font-size: 1rem;
        }
      }
    }
  }
</style>