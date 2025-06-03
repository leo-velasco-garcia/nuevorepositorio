<script setup>
    const props = defineProps({
        text : String
    })
</script>
<template>
    <h5>{{ text }}</h5>
</template>
<style scoped>
    h5{
        font-size: 1rem;
        line-height: 1.25rem;
        margin: 0.75rem 0 0.25rem 0;
        font-weight: 600;
        text-transform: uppercase;
        color: #5f5f5f;
    }

</style>