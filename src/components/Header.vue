  <script>


  export default {
    name:'Headers',
  }
  </script>


<template>

<section>
<div class="logo">
  <img src="../assets/logo.png" alt="logo">
</div>

</section>

</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as*;
@import '../scss/partials/general' ;

section{
  //colore da togliere in futuro
  background-color: $my-blue;
  height: 105px;
  .logo{
    width: 100%;
  }
}

</style>