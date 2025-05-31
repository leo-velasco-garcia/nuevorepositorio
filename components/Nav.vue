<script setup>
</script>
<template>
    <nav class="nav">
        <Boton text="close" />
    </nav>
</template>
<style scoped>
.nav {
    background-color: #F18C79;
    position: fixed;
    left: 0;
    top: 0;
    height: 100vh;
    width: 20rem;
    display: flex;
    flex-flow: column nowrap;
    gap: 1rem;
    padding: 1.75rem;
}

.nav .grupoNav {
    display: flex;
    flex-flow: column nowrap;
    /* border: 1px red solid; */
}

.nav button{
        position: absolute;
        right: 1.75rem;
        top: 1.75rem;
    }
</style>
