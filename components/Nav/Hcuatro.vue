<script setup>
    const props = defineProps({
        text : String
    })
</script>
<template>
    <a href="">
        <h4>{{ text }}</h4>
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
    a h4{
        font-size: 1.2rem;
        line-height: 1.5rem;
        font-weight: 400;
        margin: 0 0 0 1.5rem;
    }
</style>