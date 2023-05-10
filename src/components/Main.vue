  <script>
  import Platform from './partials/Platform.vue';
  import TrendingBattle from './partials/TrendingBattle.vue';
  import QuickFacts from './partials/QuickFacts.vue';
  import LiveStreaming from './partials/LiveStreaming.vue';
  import Feedback from './partials/Feedback.vue';
  import Discount from './partials/Discount.vue';
  import LatestNews from './partials/LatestNews.vue';

  export default {
    name:'Main',
    components:{
      Platform, 
      TrendingBattle,
      QuickFacts,
      LiveStreaming,
      Feedback,
      Discount,
      LatestNews
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

  <Discount />

  <LatestNews />

</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as*;

</style>