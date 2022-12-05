<template>
  <section class="card__container">
    <Card 
  v-for="home in homesInfo"
  :key="home.objectID"
  :homesInfo="home"
  />
  </section>
  
</template>

<script>
import {homes} from '@/assets/data/homes';


export default {
  
  name: 'IndexPage',
  head(){
    return {
      title : "Home"
    }
  },data(){
    return {
      homesInfo : homes
    }
  }
  
  
  
}
</script>
<style scoped>
  .card__container{
    display: flex;
    flex-wrap: wrap;
  }
</style>
