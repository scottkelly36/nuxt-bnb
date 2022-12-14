<template>
  <section class="gallery__container">
        <img v-for="(image ,i) in images" 
        :key="i" 
        :src=image alt="" 
        :class="`gallery__img${i}`"
        />
    </section>
</template>

<script>
export default {
    props : ["images"]
}
</script>

<style>
    .gallery__container{
        display: grid;
        grid-template-areas: "main one two" "main three four";
        grid-template-columns: 50% 25% 25%;
        grid-template-rows: auto;
        gap: 5px;
        
    }
    .gallery__img0{
        grid-area: main;
        width: 100%;
        height: 100%;
        border-radius: 20px 0px 0px 20px;
    }
    .gallery__img1{
        grid-area: one;
        width: 100%;
        height: 100%;
    }
    .gallery__img2{
        grid-area: two;
        width: 100%;
        height: 100%;
        border-radius: 0px 20px 0px 0px;
    }
    .gallery__img3{
        grid-area: three;
        height: 100%;
        width: 100%;
    }
    .gallery__img4{
        grid-area: four;
        height: 100%;
        width: 100%;
        border-radius: 0px 0px 20px 0px;
    }
</style>