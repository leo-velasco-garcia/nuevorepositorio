<script setup>
    definePageMeta({
        layout: 'headerless'
        })
</script>
<template>
    <div class="divlanding"> 
        <img src="/entrada.gif" alt="Logotipo de Cesida">
        <NuxtLink to="/definicion">Manual de Identidad</NuxtLink>
    </div>
</template>
<style scoped>
.divlanding{
    display: flex;
    height: 100vh;
    width: 100vw;
    justify-content: center;
    align-items: center;
    flex-flow: column nowrap;
}
img{
    width: 100vw;
    max-width: 40rem;
}
a{ 
    font-weight: 400;
    text-decoration: none ;
    transform: scale(97%);
    transition: 300ms ease-out;
    font-size: 1.2rem;
}
a:hover{
    transform: scale(100%);
    font-weight: 600;
}
* {
    font-family: "Urbanist", Avenir, Helvetica, Arial, sans-serif;
    line-height: 1.5;
    font-weight: 400;
    color: #333333;
    box-sizing: border-box;
}

.nav .enlaces .router-link-active h3 {
    color: #f18c79;
    opacity: 100%;
}
</style>