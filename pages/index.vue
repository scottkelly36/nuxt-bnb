<template>
  <Hero/>
</template>

<script>
import axios from 'axios';


export default {
  
  name: 'IndexPage',
  head(){
    return {
      title : "Home"
    }
  },
  data(){
    return{
      homes : []
    }
  }, 
  async created(){
    const config = {
      headers : {
        Accept : "application/json"
      }
    };
    try {
     
      console.log(res.data)
    } catch (error) {
      console.log(error);
    }
  }
}
</script>
