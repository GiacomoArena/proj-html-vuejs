  <script>
  import Platform from './partials/Platform.vue';
  import TrendingBattle from './partials/TrendingBattle.vue';
  import QuickFacts from './partials/QuickFacts.vue';

  export default {
    name:'Main',
    components:{
      Platform, 
      TrendingBattle,
      QuickFacts,
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

  <QuickFacts />
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as*;

</style>