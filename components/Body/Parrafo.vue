<script setup>
    const props = defineProps({
        text : String
    })
</script>
<template>
    <p>{{ text }}</p>
</template>
<style scoped>
    p{
        font-size: 1rem;
        line-height: 1.25rem;
        margin: 0 0 0.5rem 0;
    }
</style>

