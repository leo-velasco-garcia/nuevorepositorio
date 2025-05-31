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
        font-size: 2.07rem;
        line-height: 2.25rem;
        color: #F18C79;
        margin: 0 0 0.75rem 0;
    }
</style>
