  <script>
  import {quickLink,help,followUs} from '../data/db'

  export default {
    name:'Footer',
    data(){
      return{
        quickLink,
        help,
        followUs
      }
    }
  }
  </script>


<template>

  <section class="top-footer">
    <div class="futio-social">
      <img src="../assets/logo.png" alt="logo">
      <p>Lorem ipsum dolor sit amet, elit. varius enim in eros elementum Duis mi quis viverra ornare</p>
      <span><i class="fa-brands fa-youtube"></i></span>
      <span><i class="fa-brands fa-twitch"></i></span>
      <span><i class="fa-brands fa-facebook-f"></i></span>
      <span><i class="fa-brands fa-instagram"></i></span>
    </div>

    <div class="info-section">
      
      <ul>
        <h3>quick links</h3>
        <li v-for="(link,i) in quickLink" 
        :key="i">
        <a href="#">{{ link.text }}</a>
        </li>
      </ul>

      <ul>
        <h3>help</h3>
        <li v-for="(link,i) in help" 
        :key="i">
        <a href="#">{{ link.text }}</a>
        </li>
      </ul>

      <ul>
        <h3>Follow Us</h3>
        <li v-for="(link,i) in followUs" 
        :key="i">
        <a href="#">{{ link.text }}</a>
        </li>
      </ul>

      <ul>
        <h3>contact</h3>
        <li>
          <h6>location:</h6>
          <span>4 Mayfield, Buckden, PE19 5SZ</span>
        </li>
        <li>
          <h6>Phone:</h6>
          <span>(302) 555-0107</span>
        </li>
      </ul>


    </div>
  </section>

  <section class="bottom-footer">
    <p>Copyright © 2022 <span>FUTIO</span> . All rights reserved.</p>
  </section>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as*;
//da togliere e mettere succesivamente nel jumbotron
  .top-footer{
    font-family: $secondary-font;
    height: 575px;
    padding-top: 105px;
    color: white;
    background-color:$my-blue;
    display: flex;
    justify-content: space-around;
    align-items: center;
    .futio-social{
      width: 400px;
      span{
        color: $my-white;
        font-size: 1rem;
        border: 1px solid $my-white;
        margin: 5px;
        padding: 8px 11px;
        border-radius: 50%;
        cursor: pointer;
        &:hover{
          background-color: $my-lightgreen;
        }
      }
    }
    .info-section{
      display: flex;
      ul{
        width: 200px;
        list-style: none;
        li{
          margin-top: 15px;
        }
        a{
          text-decoration: none;
          color: $my-white;
          text-transform: capitalize;
          &:hover{
            color: $my-lightgreen;
          }
        }
      }
      h3{
        text-transform: capitalize;
        font-family: $primary-font;
        font-weight: 600;
        font-size: 1.5rem;
      }
      h6{
        text-transform: capitalize;
        color: $my-lightgreen;
      }
    }
    
  }
  .bottom-footer{
      display: flex;
      align-items: center;
      justify-content: center;
      height: 90px;
      background-color: #1B222E;
      color: $my-white;
      span{
        color:  $my-lightgreen;
      }
    }
</style>