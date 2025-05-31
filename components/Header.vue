<script setup>
    let num = Math.floor(Math.random() * 38) + 1;
    const logoheader = `/header/LogoCesida-${num}.svg`
</script>
<template>
    <header class="header">
        <NuxtLink to="/"><img :src="logoheader" alt="Logotipo de Cesida"></NuxtLink>
        <Boton text="menu" sol="material-symbols-outlined"/>

    </header>
</template>
<style scoped>
    .header{
        /* background-color: red; */
        /* border: 1px solid red; */
        position: fixed;
        right: 0;
        top: 0;
        width: calc(100vw - 20rem);
        height: 6.5rem;
        z-index: 999;
    }
    .header img{
        height: 2rem;
        position: absolute;
        right: 2.5rem;
        top: 50%;
        transform: translateY(-50%);
    }
    .header button{
        position: absolute;
        left: 2.5rem;
        top: 50%;
        transform: translateY(-50%);
    }
</style>
