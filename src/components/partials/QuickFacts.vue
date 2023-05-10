  <script>
  

  export default {
    name:'QuickFacts',
    data(){
      return{
        
      }
    }
  }
  </script>


<template>

<section>
  <h1>Futio Quick Facts</h1>
  <div class="containeraa">
    <div class="row justify-content-center">
      <div class="col-2 me-3 card">
        0
      </div>
      <div class="col-2 me-3 card">
        0
      </div>
      <div class="col-2 me-3 card">
        0
      </div>
      <div class="col-2 me-3 card">
        0
      </div>
    </div>
  </div>
</section>

</template>


<style lang="scss" scoped>
@use '../../scss/partials/variables' as*;
  section{
    font-family: $primary-font;
    text-align: center;
    background-color: black;
    padding: 100px 0px;
    color: white;
    .card{
      background-color: black;
      border: 1px solid #222833;
      max-width: 300px !important;
      padding: 20px;
    }
  }
</style>