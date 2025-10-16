<script setup>
import { ref, reactive, onMounted } from 'vue'
import { db } from './data/guitarras'
import Guitarra from './components/Guitarra.vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

const guitarras = ref([])
const carrito = ref([])

onMounted(() => {
    guitarras.value = db
})


const agregarCarrito = (guitarra) => {
    const existeCarrito = carrito.value.findIndex(producto => producto.id === guitarra.id)

    console.log('existe carrito')
    guitarra.cantidad = 1
    carrito.value.push(guitarra)

}

</script>

<template>
    <Header 
    :carrito="carrito" 
    />

    <main class="container-xl mt-5">
        <h2 class="text-center">Nuestra Colección</h2>
        <!-- INICIO GUITARRA -->
        <div class="row mt-5">
            <Guitarra v-for="guitarra in guitarras" :guitarra="guitarra" @agregar-carrito="agregarCarrito" />
        </div>
    </main>

    <Footer />

</template>
