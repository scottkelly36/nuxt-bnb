<template>
  <article class="card">
    
    <swiper
    :slides-per-view="3"
    :space-between="50"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide>Slide 1</swiper-slide>
    <swiper-slide>Slide 2</swiper-slide>
    <swiper-slide>Slide 3</swiper-slide>
    ...
  </swiper>
    <h2 class="card__location">{{homesInfo.location.city}}, {{homesInfo.location.country}}</h2>
  </article>
</template>

<script>
 // import Swiper core and required modules
 import { Navigation, Pagination, Scrollbar, A11y } from 'swiper';

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper';

// Import Swiper styles


// Import Swiper styles
export default {
  
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log('slide change');
    };
    return {
      onSwiper,
      onSlideChange,
      modules: [Navigation, Pagination, Scrollbar, A11y],
    };
  },props:['homesInfo']
};

</script>

<style>
    .card{ background-color: aquamarine;
    width: 30%; height: 100px;}
</style>