<template>
  <section class="property__description">
    
    <p v-for="(paragraph, i) in paragraph(description)" :key="i" class="property__paragraph">{{paragraph}}</p>
    
  </section>
</template>

<script>
export default {
    props: ["description", "note"],
    methods: {paragraph(desc){
        console.log(typeof desc)
        return desc.split("\\n")
    }}
}
</script>

<style>
    .property__paragraph{
        margin: 20px 0px;
        line-height: 1.5;
    }
</style>