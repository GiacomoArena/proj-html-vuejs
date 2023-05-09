
<script>
  import {store} from '../../data/store'
  import {games,shop,pages,blog} from '../../data/db'

export default {
  name:'HeaderLinks',
  props:{
    link:String,
  },
  data(){
    return{
      store,
      games,
      shop,
      pages,
      blog,
    }
  }
}
</script>

<template>
  
  <ul>
    <li>
      <a v-if="link === 'home'" href="#">{{link}} </a>
      <a v-else-if="link === 'contact'" href="#">{{link}} </a>
      <a v-else href="#">{{link}} <img src="../../assets/svg/c-down-arrow.svg" >

      <span class="hover-container" v-if="link === 'games'" >
        <ul v-for="(text, i) in games" :key="i">
          <li>
            <a href="#">{{text.text}}</a>
          </li>
        </ul>
      </span>
      <span class="hover-container" v-if="link === 'shop'" >
        <ul v-for="(text, i) in shop" :key="i">
          <li>
            <a href="#">{{text.text}}</a>
          </li>
        </ul>
      </span>
      <span class="hover-container" v-if="link === 'pages'" >
        <ul v-for="(text, i) in pages" :key="i">
          <li>
            <a href="#">{{text.text}}</a>
          </li>
        </ul>
      </span>
      <span class="hover-container" v-if="link === 'blog'" >
        <ul v-for="(text, i) in blog" :key="i">
          <li>
            <a href="#">{{text.text}}</a>
          </li>
        </ul>
      </span>
    
    </a>
    </li>
  </ul>

</template>

<style lang="scss" scoped>
@use '../../scss/partials/variables' as*;
ul{
  margin: 0 10px;
  list-style: none;
  
  a{
    position: relative;
    text-decoration: none;
    color: white;
    padding: 15px 0;
    &:hover{
      color: $my-lightgreen;
    }
    &:hover .hover-container{
      opacity: 1;
      display: flex;
    }
    
    
    .hover-container{
      padding: 30px 0;
      width: 200px;
      display: none;
      flex-direction: column;
      position: absolute;
      background-color: $my-blue;
      top: 40px;
      right: -60px;
      opacity: 0;
      
    }

  }
}

</style>