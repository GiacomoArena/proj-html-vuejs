
<script>
export default {
  name:'HeaderLinks',
  props:{
    link:String,
  }
}
</script>

<template>
  
  <ul>
    <li>
      <a href="#">{{link}}</a>
    </li>
  </ul>

</template>

<style lang="scss" scoped>
@use '../../scss/partials/variables' as*;
ul{
  margin: 0 10px;
  list-style: none;
  a{
    text-decoration: none;
    color: white;
  }
}

</style>