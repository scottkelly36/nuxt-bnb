<template>
  <section class="review__bar">
    <p class="property__review">{{value}}</p>
        <p class="property__spacing">.</p>
        <NuxtLink to="" class="property__reviewsCount">{{isPlural(count, "Review")}}</NuxtLink>
        <p class="property__spacing">.</p>
        <p class="property__location">{{city}}, {{country}}</p>
  </section>
</template>

<script>
export default {
    props : ["value", "count", "city", "country"],
    methods:{
        isPlural(count, word){
            console.log(typeof count)
            if(count === 1){
                return`${count} ${word}`
            } else {
                return `${count} ${word}'s`
            } 
        }
    }
}
</script>

<style>
    .review__bar{
        display: flex;
        align-items: center;
        text-align: center;
        width:100%;
        margin: 20px 0;
    }
    .property__spacing{
        display: inline;
        justify-content: center;
        align-items: center;
        width: 50px;
    }
</style>