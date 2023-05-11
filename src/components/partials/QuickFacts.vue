  <script>
  

  export default {
    name:'QuickFacts',
    data(){
      return{
        fact:4,
        factsNumber:[],
        target:[1051,58,714,67],
      }
    },
    methods:{ 
      allFacts(){
        for (let i = 0; i < this.fact; i++) {
          this.factsNumber.push(0)
        }
      },
      increaseNumber(){
        //I create a function that takes the initial number and takes it to the target value by seeing the increment through a setinterval
        
          for (let i = 0; i < this.factsNumber.length && i < this.target.length; i++) {
            const timer = setInterval(() => {
            if (this.factsNumber[i] != this.target[i]) {
              this.factsNumber[i] ++
            }
            else{
              clearInterval(timer)
            }
            
          }, 40);
          }
      }
    },
    created(){
      this.allFacts()
    }
  }
  </script>


<template>

<section @mouseover="increaseNumber()">
  <h1>Futio Quick Facts</h1>
  <div class="containeraa">
    <div class="row justify-content-center">
      <div class="col-2 me-3 card" >
        {{factsNumber[0]}}
        <h5>Twich Stream</h5>
      </div>
      <div class="col-2 me-3 card">
        {{factsNumber[1]}}
        <h5>Total Games</h5>
      </div>
      <div class="col-2 me-3 card">
        {{factsNumber[2]}}
        <h5>Youtube Streams</h5>
      </div>
      <div class="col-2 me-3 card">
        {{factsNumber[3]}}
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