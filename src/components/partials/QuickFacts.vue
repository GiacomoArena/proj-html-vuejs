  <script>
  

  export default {
    name:'QuickFacts',
    data(){
      return{
        startNumber:0,
        target:[300]
      }
    },
    methods:{ 

      increaseNumber(){
        const timer = setInterval(() => {
          for (let i = 0; i < this.target.length; i++) {
            
            if (this.startNumber != this.target) {
              this.startNumber ++
            }
            else{
              clearInterval(timer)
            }
            
          }
        }, 50);
      }
    },
    mounted(){
      
    }
  }
  </script>


<template>

<section @mouseover="increaseNumber()">
  <h1>Futio Quick Facts</h1>
  <div class="containeraa">
    <div class="row justify-content-center">
      <div class="col-2 me-3 card" >
        {{startNumber}}
        <h5>Twich Stream</h5>
      </div>
      <div class="col-2 me-3 card">
        {{startNumber}}
        <h5>Total Games</h5>
      </div>
      <div class="col-2 me-3 card">
        {{startNumber}}
        <h5>Youtube Streams</h5>
      </div>
      <div class="col-2 me-3 card">
        {{startNumber}}
        <h5>Pro Team</h5>
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
    h1{
      padding-bottom: 40px;
      font-size: 3rem;
      font-weight: 600;
    }
    .card{
      background-color: black;
      border: 1px solid #222833;
      max-width: 300px !important;
      padding: 25px;
      font-size: 2.8rem;
      font-weight: 600;
      border-radius: 40px;
      transition: all 1s;
      h5{
        color: $my-lightgreen;
        font-size: .8rem;
        font-weight: 600;
      }
    }
  }
</style>