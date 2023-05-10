  <script>
  

  export default {
    name:'LatestNews',
    data(){
      return{
        
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
  </section>
</template>


<style lang="scss" scoped>
@use '../../scss/partials/variables' as*;
  section{
    padding-bottom: 200px;
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
  }
</style>