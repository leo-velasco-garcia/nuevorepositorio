<script setup>
    const props = defineProps({
        text : String
    })
</script>
<template>
    <h3>{{ text }}</h3>
</template>
<style scoped>
    h3{
        font-size: 1.44rem;
        line-height: 1.75rem;
        font-weight: 400;
        margin: 0;
        text-decoration: none;
        color: white;
        opacity: 80%;
        transition: 300ms ease-out;
    }
    h3:hover{
        opacity: 100%;
        font-weight: 600;
    }
</style>