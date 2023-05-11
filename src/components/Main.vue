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


<template >
  <!-- I create a $emit that will change the value of a flag for me that is used to make the button that sends you to the top page visible or not -->
  <section @mouseover="$emit('scrollfalse')">
    <!-- I create partials that will then be called here on the main  -->
    <Platform />
  
    <TrendingBattle />
  
    <QuickFacts />
  
    <LiveStreaming />
  
    <Feedback />
  
    <Discount />
  
    <LatestNews />
  </section>

</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as*;

</style>