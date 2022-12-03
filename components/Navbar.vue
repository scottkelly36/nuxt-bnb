<template>
  <nav class="navbar__desktop">
    <div class="logo__container">
        <p class="logo--small">
            Nuxt BNB
        </p>
    </div>
    <ul class="navbar__links">
        <li class="navbar__link"><nuxt-link to="/">Home</nuxt-link></li>
        <li class="navbar__link"><nuxt-link to="/">Login</nuxt-link></li>
    </ul>
  </nav>
</template>

<script>
export default {

}
</script>

<style>
    .navbar__desktop{
        width: 100%;
        height: 50px;
        display: flex;
        background-color: #000080;
        justify-content: space-between;
    }
    .logo__container{
        width: 100px;
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
    }
    .logo--small{
        font-size: 1.2rem;
    }
    .navbar__links{
        display: flex;
        width: 40%;
        justify-content: space-around;
        align-items: center;
        list-style: none;
    }
    .navbar__link a{
        color: white; 
        text-decoration: none;
    }
</style>