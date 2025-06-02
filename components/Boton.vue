<script setup>
    const props = defineProps({
        text : String,
        sol : String
    })
</script>

<template>
    <button>
        <span :class="sol">
            {{ text }}
        </span>
    </button>
</template>

<style scoped>
    button{
        border: 0;
        transition: 200ms ease-in-out;
        padding: 0;
        opacity: 50%;
        background-color: #00000000;
    }
    button:hover{
        opacity: 100%;
    }
    /* button span{
        color: red;
    } */
    .blanco{
        color: white;
    }
    .red{
        color: red;
    }
    .none{
        display: none;
    }
</style>