<template>
  <section class="property__hosts">
    <h2 class="host__title">{{type}} hosted by {{host.name}}</h2>
    <article class="hosts__info">
        <p class="host__guest-count">{{isPlural(guests, "Guest")}}</p>
        <p class="property__spacing">.</p>
        <p class="hosts__room-count">{{isPlural(bedrooms, "Bedroom")}}</p>
        <p class="property__spacing">.</p>
        <p class="hosts__bed-count">{{isPlural(beds, "Bed")}}</p>
        <p class="property__spacing">.</p>
        <p class="hosts__bathroom-count">{{isPlural(bathrooms, "Bathroom")}}</p>
        <img :src="host.image" alt="" class="hosts__image--small">
    </article>
    
    
  </section>
</template>

<script>
export default {
    props:[
    "type",
     "guests",
     "bedrooms",
     "bathrooms",
     "beds",
     "host"
    ],
    methods :{
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
    .hosts__info{
        display: flex;
        
        align-items: center;
        text-align: center;
    }
    .hosts__image--small{
        border-radius:50%;
        width: 75px;
        height: 75px;
    }
</style>