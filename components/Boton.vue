<script setup>
    const props = defineProps({
        text : String,
        colorBoton : String
    })
</script>

<template>
    <button>
        <span class="material-symbols-outlined">
            {{ text }}
        </span>
    </button>
</template>

<style scoped>
    button{
        background-color: #00000000;
        border: 0;
        color: #333333;
        transition: 200ms ease-in-out;
        padding: 0;
        opacity: 60%;
    }
    button:hover{
        color: #333333;
        opacity: 100%;
    }
</style>