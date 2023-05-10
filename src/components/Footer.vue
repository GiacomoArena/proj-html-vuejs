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
    <div class="newsletter">
      <span>
        <h3>Subscribe Newsletter</h3>
        <p>
          libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus.
        </p>
      </span>
      <div class="input-container">
        <input type="email" placeholder="Enter your email">
        <img src="../assets/icon/send-icon.png" alt="icon">
      </div>
    </div>

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
    position: relative;
    font-family: $secondary-font;
    height: 575px;
    color: white;
    background-color:#283449;
    display: flex;
    justify-content: space-around;
    align-items: center;
    .newsletter{
      font-family: $secondary-font;
      padding: 60px;
      width: 80%;
      border-radius: 25px;
      max-width: 1100px;
      position: absolute;
      color: white;
      top: -150px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      background-color: $my-blue;
      h3{
        font-family: $primary-font;
        font-size: 2.3rem;
        font-weight: 600;
      }
      span{
        width: 50%;
      }
      .input-container{
        position: relative;
        input{
          padding: 10px;
          color: $my-white;
          width: 300px;
          height: 60px;
          border-radius: 15px;
          background-color: #425374;
          border: 1px solid #6e798f;
          &:focus{
            border-color: $my-lightgreen;
            outline: none;
          }
        }
        img{
          padding: 7px;
          border-radius: 50%;
          position: absolute;
          right: 15px;
          bottom: 10px;
          background-color: $my-lightgreen;
          cursor: pointer;
        }
      }
    }
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
      background-color: $my-darkblue;
      color: $my-white;
      span{
        color:  $my-lightgreen;
      }
    }
</style>