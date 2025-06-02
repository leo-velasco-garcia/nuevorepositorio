<script setup>
    const props = defineProps({
        text : String,
        ident : String
    })
</script>
<template>
    <h3 :id="ident">{{ text }}</h3>
</template>
<style scoped>
    h3{
        font-size: 1.72rem;
        line-height: 2rem;
        margin: 2rem 0 0.5rem 0;
        font-weight: 600;
    }
</style>
