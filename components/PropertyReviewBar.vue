<template>
  <section class="review__bar">
    <p class="property__review">{{value}}</p>
        <p class="property__spacing"></p>
        <NuxtLink to="" class="property__reviewsCount">{{isPlural(count, "Review")}}</NuxtLink>
        <p class="property__spacing"></p>
        <p class="property__location">{{city}}, {{country}}</p>
  </section>
</template>

<script>
export default {
    props : ["value", "count", "city", "country"],
    methods:{
        isPlural(count, word){
            
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
        width: 5px;
        height: 5px;
        background-color: var(--black);
        border-radius: 50%;
        margin: 0px 15px;
    }
</style>