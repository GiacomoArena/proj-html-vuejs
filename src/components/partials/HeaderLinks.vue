
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

            <a v-if="text.text === 'team'" href="#">
              {{text.text}}
              <i class="fa-solid fa-caret-right"></i>
              <ul class="insider-link">
                <li><a href="#">All Team</a></li>
                <li><a href="#">Team Details</a></li>
              </ul>
            </a>

            <a v-else-if="text.text === 'player'" href="#">
              {{text.text}}
              <i class="fa-solid fa-caret-right"></i>
              <ul class="insider-link">
                <li><a href="#">Players</a></li>
                <li><a href="#">Players Single</a></li>
              </ul>
            </a>

            <a v-else href="#">{{text.text}}</a>
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
    transition: all 0.1s;
    &:hover{
      color: $my-lightgreen;
    }
    &:hover .hover-container{
      opacity: 1;
      display: flex;
    }
    
    
    .hover-container{
      
      line-height: 35px;
      padding: 18px 0px;
      width: 200px;
      display: none;
      flex-direction: column;
      position: absolute;
      background-color: $my-darkblue;
      top: 40px;
      right: -60px;
      opacity: 0;
      a:hover .insider-link{
        opacity: 1;
      } 
      .insider-link{
        position: absolute;
        width: 200px;
        background-color: $my-darkblue;
        left: 150px;
        top: 15px;
        opacity: 0;
      }
    }

  }
}

</style>