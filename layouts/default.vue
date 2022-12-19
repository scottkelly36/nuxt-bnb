<template>
    <div>
    <Navbar/>
    <div class="page__wrapper">
        <Nuxt/>  
    </div>
    
    </div>
    
</template>
<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;500&display=swap');
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Open Sans', sans-serif;
}

:root{
    --black: rgba(49, 54, 57, 1);
    --grey: rgba(211, 211, 211,1);
    --blue:#000080;
}

.page__wrapper{
    padding: 25px 300px;
}
</style>