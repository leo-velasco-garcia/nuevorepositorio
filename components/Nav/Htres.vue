<script setup>
    const props = defineProps({
        text : String
    })
</script>
<template>
    <a href="">
        <h3>{{ text }}</h3>
    </a>
</template>
<style scoped>
    a{
        text-decoration: none;
        color: #333;
        opacity: 80%;
        transition: 200ms ease-in-out;
    }
    a:hover{
        opacity: 100%;
    }
    a h3{
        font-size: 1.44rem;
        line-height: 1.75rem;
        font-weight: 600;
        margin: 0;
    }
</style>