  <script>
  import Platform from './partials/Platform.vue';
  import TrendingBattle from './partials/TrendingBattle.vue';

  export default {
    name:'Main',
    components:{
      Platform, 
      TrendingBattle,
    },
    data(){
      return{
        
      }
    }
  }
  </script>


<template>
  <Platform />

  <TrendingBattle />

</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as*;

</style>