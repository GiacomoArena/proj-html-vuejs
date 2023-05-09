
<script>
export default {
  name:'HeaderLinks',
  props:{
    link:String,
  },
}
</script>

<template>
  
  <ul>
    <li>
      <a v-if="link === 'home'" href="#">{{link}} </a>
      <a v-else-if="link === 'contact'" href="#">{{link}} </a>
      <a v-else href="#">{{link}} <img src="../../assets/svg/c-down-arrow.svg" ></a>
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