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
        font-size: 1.44rem;
        line-height: 1.75rem;
        margin: 0.75rem 0 0.25rem 0;
        font-weight: 500;
        /* color: #5f5f5f; */
    }

</style>
