<template>
    <section class="property__container">
        
        <Title 
        :title="homeInfo[0].title" 
        className="property__title--large"/>
        <PropertyReviewBar 
        :value="homeInfo[0].reviewValue" 
        :count="homeInfo[0].reviewCount" 
        :city="homeInfo[0].location.city" 
        :country="homeInfo[0].location.country"
        />

        <PropertyGallery 
        :images="homeInfo[0].images"/>

        <HostSection 
        :type="homeInfo[0].type" 
        :guests="homeInfo[0].guests" 
        :bedrooms="homeInfo[0].bedrooms" 
        :beds="homeInfo[0].beds" 
        :bathrooms="homeInfo[0].bathrooms" 
        :host="homeInfo[0].host"/>
        
        <PropertyDescription 
        :description="homeInfo[0].description"
        :note="homeInfo[0].note"
        />
        <DatePicker/>

    </section >
  
</template>

<script>
import {homes} from '@/assets/data/homes';
import PropertyReviewBar from '../../components/PropertyReviewBar.vue';



export default {
  components: { PropertyReviewBar },
    data(){
        return {
            homeInfo :  homes.filter((home)=>{return home.objectID === this.$route.params.id})
        }
    }
}
</script>

<style>

</style>