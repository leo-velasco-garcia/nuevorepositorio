<script setup>
    import { ref, provide, computed } from 'vue';
    const estaabiertoelnav = ref(true);
    provide('estaabiertoelnav', estaabiertoelnav)
    const anchobody = computed(() => estaabiertoelnav.value ? 'secnormal' : 'secnormal ancha');
</script>
<template>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Urbanist:ital,wght@0,100..900;1,100..900&display=swap"
        rel="stylesheet">
    <link rel="stylesheet"
        href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200" />
    <div>
        <Nav />
        <Header />
        <div :class="anchobody">
            <div class="centradora">
                <slot/>
            </div>
        </div>
    </div>
    
</template>
<style>
* {
    font-family: "Urbanist";
    line-height: 1.5;
    font-weight: 400;
    color: #333333;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

.nav .enlaces .router-link-active h3 {
    color: #f18c79;
    opacity: 100%;
}

.secnormal{
        display: flex;
        height: calc(100vh - 6.75rem);
        overflow-y: scroll;
        margin: 0;
        /* border: 1px salmon solid; */
        /* justify-content: center; */
        /* padding: 2rem; */
        /* background-color: #f18c79; */
        justify-content: center;
        width: calc(100vw - 20rem);
        position: absolute;
        right: 0;
        top: 6.5rem;
        scroll-behavior: smooth;
    }

.ancha {
    width: 100vw;
}
.secnormal .centradora{
    display: flex;
    flex-flow: column;
    padding: 2.5rem;
    width: 100%;
    align-items: start;
    background-color: white;
    max-width: 60rem;
    height: fit-content;
}
</style>