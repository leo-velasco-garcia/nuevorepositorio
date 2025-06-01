<script setup>
    const props = defineProps({
        text : String,
        alt : String,
    })
</script>
<template>
    <img :src="text" :alt="alt">
</template>
<style scoped>
    img{
        max-height: calc(100vh - 5rem);
        width: 100%;
        border: 1px solid #333333;
        border-radius: 0.5rem;
        margin: 0 0 3.5rem 0;
    }
</style>
