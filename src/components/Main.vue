  <script>
  import Platform from './partials/Platform.vue';
  import TrendingBattle from './partials/TrendingBattle.vue';
  import QuickFacts from './partials/QuickFacts.vue';
  import LiveStreaming from './partials/LiveStreaming.vue';
  import Feedback from './partials/Feedback.vue';

  export default {
    name:'Main',
    components:{
      Platform, 
      TrendingBattle,
      QuickFacts,
      LiveStreaming,
      Feedback
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

  <LiveStreaming />

  <Feedback />

</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as*;

</style>