<script setup>
    const props = defineProps({
        text : String
    })
</script>
<template>
    <h2>{{ text }}</h2>
</template>
<style scoped>
    h2{
        color: white;
        font-size: 1rem;
        text-transform: uppercase;
        font-weight: 600;
        margin: 0;
    }
</style>