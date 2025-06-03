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
                <NuxtLink style="text-decoration: none;" to="/marca">
                    <NavHtres text="Marca" />
                </NuxtLink>
                <div class="subapartados" v-if="$route.path === '/marca'" subenlacesdefinicion>
                    <a class="subenlace" href="/marca#concepto">Concepto</a>
                    <a class="subenlace" href="/marca#construccion">Construcción</a>
                    <a class="subenlace" href="/marca#areaderespeto">Área de respeto</a>
                    <a class="subenlace" href="/marca#variantes">Variantes</a>
                    <a class="subenlace" href="/marca#minimos">Tamaños mínimos</a>
                </div>
                <NuxtLink style="text-decoration: none;" to="/submarca">
                    <NavHtres text="Submarca" />
                </NuxtLink>
                <div class="subapartados" v-if="$route.path === '/submarca'" subenlacesdefinicion>
                    <a class="subenlace" href="/submarca#construccionsub">Construcción</a>
                    <a class="subenlace" href="/submarca#versionreducida">Versión reducida</a>
                    <a class="subenlace" href="/submarca#tipografiapride">Tipografía</a>
                    <a class="subenlace" href="/submarca#colorpride">Color</a>
                    <a class="subenlace" href="/submarca#positivopride">Positivo y negativo</a>
                    <a class="subenlace" href="/submarca#imgpride">Tratamiento de imagen</a>
                    <a class="subenlace" href="/submarca#aplicacionespride">Aplicaciones</a>
                </div>
                <NuxtLink style="text-decoration: none;" to="/tipografia">
                    <NavHtres text="Tipografía" />
                </NuxtLink>
                <div class="subapartados" v-if="$route.path === '/tipografia'" subenlacesdefinicion>
                    <a class="subenlace" href="/tipografia#textocorrido">Texto corrido</a>
                    <a class="subenlace" href="/tipografia#estilosweb">Versión reducida</a>
                    <a class="subenlace" href="/tipografia#comportipo">Tipografía</a>
                </div>
                <NuxtLink style="text-decoration: none;" to="/color">
                    <NavHtres text="Color" />
                </NuxtLink>
                <div class="subapartados" v-if="$route.path === '/color'" subenlacesdefinicion>
                    <a class="subenlace" href="/color#psicologia">Psicología</a>
                    <a class="subenlace" href="/color#colorcorporativo">Color corporativo</a>
                    <a class="subenlace" href="/color#coloressecundarios">Colores secundarios</a>
                    <a class="subenlace" href="/color#escalagrises">Escala de grises</a>
                </div>
                <NuxtLink style="text-decoration: none;" to="/espaciado">
                    <NavHtres text="Espaciado" />
                </NuxtLink>
                <div class="subapartados" v-if="$route.path === '/espaciado'" subenlacesdefinicion>
                    <a class="subenlace" href="/espaciado#usomargenes">Uso de márgenes</a>
                    <a class="subenlace" href="/espaciado#reticulas">Retículas</a>
                    <a class="subenlace" href="/espaciado#usomargenvideo">Uso de márgenes en vídeo</a>
                </div>
                <NuxtLink style="text-decoration: none;" to="/imagen">
                    <NavHtres text="Imagen" />
                </NuxtLink>
                <div class="subapartados" v-if="$route.path === '/imagen'" subenlacesdefinicion>
                    <a class="subenlace" href="/imagen#tipoimg">Tipo de imagen</a>
                    <a class="subenlace" href="/imagen#tratamientoimg">Tratamiento de imagen</a>
                </div>
                <NuxtLink style="text-decoration: none;" to="/graficos">
                    <NavHtres text="Gráficos" />
                </NuxtLink>
                <div class="subapartados" v-if="$route.path === '/graficos'" subenlacesdefinicion>
                    <a class="subenlace" href="/graficos#formas">Formas</a>
                    <a class="subenlace" href="/graficos#patrones">Patrones</a>
                    <a class="subenlace" href="/graficos#iconos">Iconos</a>
                </div>
                <NuxtLink style="text-decoration: none;" to="/movimiento">
                    <NavHtres text="Movimiento" />
                </NuxtLink>
                <div class="subapartados" v-if="$route.path === '/movimiento'" subenlacesdefinicion>
                    <a class="subenlace" href="/movimiento#fisicas">Físicas</a>
                    <a class="subenlace" href="/movimiento#sistema">Sistema</a>
                    <a class="subenlace" href="/movimiento#timing">Timing</a>
                    <a class="subenlace" href="/movimiento#muestras">Muestras</a>
                </div>
                <NuxtLink style="text-decoration: none;" to="/aplicaciones">
                    <NavHtres text="Aplicaciones" />
                </NuxtLink>
                <div class="subapartados" v-if="$route.path === '/aplicaciones'" subenlacesdefinicion>
                    <a class="subenlace" href="/aplicaciones#estaticas">Estáticas</a>
                    <a class="subenlace" href="/aplicaciones#dinamicas">Dinámicas</a>
                    <a class="subenlace" href="/aplicaciones#web">Web</a>
                </div>
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
    width: 100vw;
    display: flex;
    flex-flow: column nowrap;
    justify-content: space-between;
    padding: 2.5rem;
    gap: 1rem;
    transition: 200ms ease-out;
    z-index: 1099;
}

@media (min-width: 760px) {
    .nav{
        max-width: 20rem;
    }
  /* … */
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