<script setup>
import { ref, computed, inject } from 'vue';
import { useRoute } from 'vue-router'

const estaabiertoelnav = inject('estaabiertoelnav')
const displayequis = computed(() => estaabiertoelnav.value ? 'material-symbols-outlined blanco' : 'material-symbols-outlined blanco none');
const displaynav = computed(() => estaabiertoelnav.value ? 'nav' : 'nav nomuestra');
function togglePatata() {
    estaabiertoelnav.value = !estaabiertoelnav.value
}

const route = useRoute()
const subapartados = {
    '/aplicaciones': [
        { id: 'estaticas', label: 'Estáticas' },
        { id: 'dinamicas', label: 'Dinámicas' },
        { id: 'web', label: 'Web' }
    ],
    '/color': [
        { id: 'psicologia', label: 'Psicología del color' },
        { id: 'colorcorporativo', label: 'Color corporativo' },
        { id: 'coloressecundarios', label: 'Colores secundarios' },
        { id: 'escalagrises', label: 'Escala de grises' }
    ],
    '/definicion': [
        { id: 'intro', label: 'Introducción e intención' },
        { id: 'valores', label: 'Valores' },
        { id: 'tono', label: 'Tono' }
    ],
    '/espaciado': [
        { id: 'usomargenes', label: 'Uso de márgenes y tamaños mínimos' },
        { id: 'reticulas', label: 'Retículas' },
        { id: 'usomargenvideo', label: 'Uso de márgenes en vídeo' }
    ],
    '/graficos': [
        { id: 'formas', label: 'Formas' },
        { id: 'patrones', label: 'Patrones' },
        { id: 'iconos', label: 'Iconos' }
    ],
    '/imagen': [
        { id: 'tipoimg', label: 'Tipo de imagen' },
        { id: 'tratamientoimg', label: 'Tratamiento de imagen' }
    ],
    '/marca': [
        { id: 'concepto', label: 'Concepto' },
        { id: 'construccion', label: 'Construcción' },
        { id: 'areaderespeto', label: 'Área de respeto' },
        { id: 'variantes', label: 'Variantes' },
        { id: 'minimos', label: 'Tamaños mínimos' },
    ],
    '/movimiento': [
        { id: 'fisicas', label: 'Físicas' },
        { id: 'sistema', label: 'Sistema' },
        { id: 'timing', label: 'Timing' }
    ],
    '/submarca': [
        { id: 'construccion', label: 'Construcción' },
        { id: 'versionreducida', label: 'Versión reducida' },
        { id: 'tipografiapride', label: 'Tipografía' },
        { id: 'colorpride', label: 'Tipografía +Pride Positivo' },
        { id: 'postivopride', label: 'Positivo y negativo' },
        { id: 'imgpride', label: 'Tratamiento de imagen' },
        { id: 'aplicacionespride', label: 'Aplicaciones' },
    ],
    '/tipografia': [
        { id: 'textocorrido', label: 'Texto corrido' },
        { id: 'estilosweb', label: 'Estilos web' },
        { id: 'comportipo', label: 'Comportamiento en aplicaciones estáticas' }
    ],
}
const apartadosVisibles = computed(() => {
    return subapartados[route.path]
})

</script>
<template>
    <nav :class="displaynav">
        <Boton text="close" :sol="displayequis" @click="togglePatata" />
        <div class="arriba">
            <NavHdos text="Manual de marca" />
            <div class="enlaces">
                <NuxtLink style="text-decoration: none;" to="/definicion">
                    <NavHtres text="Definición" />
                </NuxtLink>
                <div class="subapartados" v-if="$route.path === '/definicion'" subenlacesdefinicion>
                    <a class="subenlace" href="/definicion#intro">Intro</a>
                    <a class="subenlace" href="/definicion#valores">Valores</a>
                    <a class="subenlace" href="/definicion#tono">Tono</a>
                </div>
                <NuxtLink style="text-decoration: none;" to="/submarca">
                    <NavHtres text="Submarca" />
                </NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/tipografia">
                    <NavHtres text="Tipografía" />
                </NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/color">
                    <NavHtres text="Color" />
                </NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/espaciado">
                    <NavHtres text="Espaciado" />
                </NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/imagen">
                    <NavHtres text="Imagen" />
                </NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/graficos">
                    <NavHtres text="Gráficos" />
                </NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/movimiento">
                    <NavHtres text="Movimiento" />
                </NuxtLink>
                <NuxtLink style="text-decoration: none;" to="/aplicaciones">
                    <NavHtres text="Aplicaciones" />
                </NuxtLink>
            </div>
        </div>
        <div class="nombres">
            <NavHdos text="Daniel Aznar" />
            <NavHdos text="Jorge Blas" />
            <NavHdos text="Leo Velasco" />
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

.nav .subapartados {
    display: flex;
    flex-flow: column;
    margin: 0 0 0.5rem 0;
}
.nav .subapartados .subenlace{
    text-decoration: none;
    color: #cacaca;
    transition: 200ms ease-out;
    padding-left: 1rem;
}
.nav .subapartados .subenlace:hover{
    color: white;
}

.nav .arriba {
    display: flex;
    flex-flow: column;
    gap: 1rem;
}

.nav .arriba .enlaces {
    display: flex;
    flex-flow: column;
    gap: 0.25rem;
}

.nav .nombres {
    display: flex;
    flex-flow: column;
}

.nav button {
    position: absolute;
    right: 2.5rem;
    top: 2.5rem;
}

.nav button .equis {
    color: white;
    background-color: white;
}

.nomuestra {
    transform: translateX(-150vw);
}
</style>