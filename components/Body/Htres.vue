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
        font-size: 1.72rem;
        line-height: 2rem;
        margin: 0.5rem 0 0.5rem 0;
    }
</style>
