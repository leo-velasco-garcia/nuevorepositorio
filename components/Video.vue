<script setup>
    const props = defineProps({
        text : String
    })
</script>
<template>
    <iframe :src="text" allow="autoplay"></iframe>
</template>
<style scoped>
    iframe{
        max-height: calc(100vh - 5rem);
        width: 100%;
        aspect-ratio: 1.77;
        border: 1px solid #333333;
        border-radius: 0.5rem;
        margin: 0 0 3.5rem 0;

    }
</style>
