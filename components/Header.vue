<script setup>
    import { inject } from 'vue';
    const patata = inject('patata')

    let num = Math.floor(Math.random() * 38) + 1;
    const logoheader = `/header/LogoCesida-${num}.svg`;

    function togglePatata() {
        patata.value = !patata.value
    }
</script>
<template>
    <header class="header">
        <NuxtLink to="/"><img :src="logoheader" alt="Logotipo de Cesida"></NuxtLink>
        <Boton text="menu" sol="material-symbols-outlined" @click="togglePatata"/>
        <p>Header - ¿Es patata? {{ patata }}</p>

    </header>
</template>
<style scoped>
.header {
    /* background-color: red; */
    /* border: 1px solid red; */
    position: fixed;
    right: 0;
    top: 0;
    width: calc(100vw - 20rem);
    height: 6.75rem;
    z-index: 999;
    background-color: white;
}

.header img {
    height: 2rem;
    position: absolute;
    right: 2.5rem;
    top: 50%;
    transform: translateY(-50%);
}

.header button {
    position: absolute;
    left: 2.5rem;
    top: 50%;
    transform: translateY(-50%);
}
</style>
