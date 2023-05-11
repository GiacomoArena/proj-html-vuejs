  <script>
  

  export default {
    name:'LiveStreaming',
    data(){
      return{
      }
    },
    methods:{ 

    },
    mounted(){
      
    }
  }
  </script>


<template>
<section>
  <div class="text-section">
    <span>Live Streaming</span>
    <h1>Watch The Streams</h1>
    <p>
      libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Cras ultricies ligula sed magna dictum porta.
    </p>
  </div>
  <div class="live-section">
    <!-- the background is in the background -->
    <button>
      <img src="../../assets/icon/live-icon.png">
      Live
    </button>
    <div class="play">
      <a href="https://www.youtube.com/watch?v=Djz8Nc0Qxwk" >
          <img class="play" src="../../assets/icon/play-icon.png" alt="play">
        </a>
        <p>
          League Of Legends
        </p>
    </div>

    <p class="view-like">
      <span>356,599</span> Viewers
      <span>23,599</span> Likes
    </p>
  </div>
</section>

</template>


<style lang="scss" scoped>
@use '../../scss/partials/variables' as*;
  
  section{
    font-family: $primary-font;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    min-height: 600px;
    background-color: black;
    background-image: url(../../assets/live-streaming-bg.png);
    background-repeat: no-repeat;
    background-size: contain;
    text-align: center;
    .text-section{
      margin: 100px 0;
      width: 700px;
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
    .live-section{
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      font-family: $secondary-font;
      width: 1000px;
      height: 600px;
      background-image: url(../../assets/video-bg.png);
      image-rendering: optimizeQuality;
      background-repeat: no-repeat;
      background-size:100%;
      button{
        position: absolute;
        padding: 5px 20px;
        background-color: $my-orange;
        border: none;
        border-radius: 20px;
        right: 30px;
        top: 40px;
      }
      .view-like{
        position: absolute;
        bottom: 60px;
        left: 10px;
        font-size: 1.1rem;
        span{
          margin-left: 30px;
          font-size: 1.1rem;
          color: $my-lightgreen;
        }
      }
      .play{
        font-family: $primary-font;
        p{
          margin: 30px;
          font-size: 1.4rem;
          font-weight: 600;
        }
        a{
          width: 50px;
          height: 50px;
          position: relative;
          padding: 20px;
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
          border: 0.5px solid $my-green;
          border-radius: 50%;
          transform: scale(1.1);
          transition: transform 0.2s ease-out;
          z-index: 1;
        &{
          transform: scale(0.9);
          animation: pulse 1s infinite alternate ease-in-out;
        }
        @keyframes pulse {
          0% {
            transform: scale(1.3);
          }
          100% {
            transform: scale(1.1);
          }
        }
      }
          }
        }
      }
  }
</style>