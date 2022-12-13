<template>
  <article class="card">
   
      <div :pagination="true" class="swiper mySwiper" ref="swiper">
          <div class="swiper-wrapper">
          <div class="swiper-slide" v-for="(img, i) in homesInfo.images" :key="i">
             <img  :src=img alt="" class="card__img"/>
          </div>
        </div>
        <div class="swiper-button-next"></div>
        <div class="swiper-button-prev"></div>
        <div class="swiper-pagination"></div>
      </div>
   
    
    <h2 class="card__location">{{homesInfo.location.city}}, {{homesInfo.location.country}}</h2>
    <p class="text--light">{{homesInfo.title}}</p>
    <p class="text--heavy card__price">£{{homesInfo.pricePerNight}}</p>
  </article>
</template>

<script>

import Swiper from 'swiper/swiper-bundle.min';
import 'swiper/swiper-bundle.min.css';


export default {
  async mounted() {
    await this.$nextTick();
    new Swiper(this.$refs.swiper, {
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },pagination: {
    el: '.swiper-pagination',
  },
    });
  },
 props:['homesInfo'],


 
 
};


</script>

<style>



    .card{ 
      
      width: 25%;
      height: fit-content;
      margin: 25px;
    }

    .card:hover{
      scale: 1.1;
    }

    .card__img{
      width: 100%;
      border-radius: 10px;
    }

    .card__price{
      text-decoration: underline;
    }
</style>