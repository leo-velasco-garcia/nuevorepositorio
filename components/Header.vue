<script setup>
    import { ref, computed, inject } from 'vue';
    const estaabiertoelnav = inject('estaabiertoelnav')
    const displayburger = computed(() => estaabiertoelnav.value ? 'material-symbols-outlined none' : 'material-symbols-outlined');
    const anchoheader = computed(() => estaabiertoelnav.value ? 'header' : 'header ancho');

    let num = Math.floor(Math.random() * 38) + 1;
    const logoheader = `/header/LogoCesida-${num}.svg`;

    function togglePatata() {
        estaabiertoelnav.value = !estaabiertoelnav.value
    } 
</script>
<template>
    <header :class="anchoheader">
        <NuxtLink to="/"><img :src="logoheader" alt="Logotipo de Cesida"></NuxtLink>
        <Boton text="menu" :sol="displayburger" @click="togglePatata"/>

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

.ancho{
    width: 100vw;
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
