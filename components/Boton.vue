<script setup>
    const props = defineProps({
        text : String
    })
</script>

<template>
    <button>
        <span class="material-symbols-outlined equis">
            {{ text }}
        </span>
    </button>
</template>

<style scoped>
    button{
        border: 0;
        transition: 200ms ease-in-out;
        padding: 0;
        opacity: 80%;
        background-color: #00000000;
    }
    button:hover{
        opacity: 100%;
    }
    /* button span{
        color: red;
    } */
</style>