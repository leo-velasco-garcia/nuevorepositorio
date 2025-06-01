<script setup>
    const props = defineProps({
        text : String
    })
</script>
<template>
    <h4>{{ text }}</h4>
</template>
<style scoped>
    h4{
        font-size: 1rem;
        line-height: 1.25rem;
        margin: 0.75rem 0 0.25rem 0;
        font-weight: 600;
        text-transform: uppercase;
        color: #5f5f5f;
    }

</style>
