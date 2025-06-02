<script setup>
    import { ref, computed, inject } from 'vue';
    const estaabiertoelnav = inject('estaabiertoelnav')
    const displayequis = computed(() => estaabiertoelnav.value ? 'material-symbols-outlined blanco' : 'material-symbols-outlined blanco none');
    const displaynav = computed(() => estaabiertoelnav.value ? 'nav' : 'nav nomuestra');
    function togglePatata() {
        estaabiertoelnav.value = !estaabiertoelnav.value
    }
</script>
<template>
    <nav :class="displaynav">
        <Boton text="close" :sol="displayequis" @click="togglePatata"/>
        <div class="arriba">
            <NavHdos text="Manual de marca"/>
            <div class="enlaces">
                <NuxtLink style="text-decoration: none;" to="/definicion"><NavHtres text="Definición"/></NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/marca"><NavHtres text="Marca"/></NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/submarca"><NavHtres text="Submarca"/></NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/tipografia"><NavHtres text="Tipografía"/></NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/color"><NavHtres text="Color"/></NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/espaciado"><NavHtres text="Espaciado"/></NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/imagen"><NavHtres text="Imagen"/></NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/graficos"><NavHtres text="Gráficos"/></NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/movimiento"><NavHtres text="Movimiento"/></NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/aplicaciones"><NavHtres text="Aplicaciones"/></NuxtLink>
            </div>
        </div>
        <div class="nombres">
            <NavHdos text="Daniel Aznar"/>
            <NavHdos text="Jorge Blas"/>
            <NavHdos text="Leo Velasco"/>
        </div>
    </nav>
</template>
<style scoped>
    .nav {
        background-color: #333333;
        position: fixed;
        left: 0;
        top: 0;
        height: 100vh;
        width: 20rem;
        display: flex;
        flex-flow: column nowrap;
        justify-content: space-between;
        padding: 2.5rem;
        gap: 1rem;
        transition: 200ms ease-out;
    }
    .nav .arriba{
        display: flex;
        flex-flow: column;
        gap: 1rem;
    }
    .nav .arriba .enlaces{
        display: flex;
        flex-flow: column;
        gap: 0.25rem;
    }
    .nav .nombres{
        display: flex;
        flex-flow: column;
    }
    .nav button{
        position: absolute;
        right: 2.5rem;
        top: 2.5rem;
    }
    .nav button .equis{
        color: white;
        background-color: white;
    }
    
    .nomuestra{
        transform: translateX(-150vw);
    }

</style>

