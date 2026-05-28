<template>
  <div class="container mt-5">
    <h2>Catálogo de Productos</h2>
    
    <div class="mb-4">
      <input 
        v-model="busqueda" 
        type="text" 
        class="form-control" 
        placeholder="Buscar producto por nombre..."
      >
    </div>

    <div class="row">
      <div class="col-md-4 mb-4" v-for="producto in productosFiltrados" :key="producto.id">
        <div class="card shadow-sm">
          <div class="card-body">
            <h5 class="card-title">{{ producto.nombre }}</h5>
            <p class="card-text">${{ producto.precio }}</p>
            <router-link :to="`/catalogo/${producto.id}`" class="btn btn-primary btn-sm">
              Ver Detalles
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed, onMounted } from 'vue'
import axios from 'axios'

const productos = ref([])
const busqueda = ref('')

// Filtrado reactivo en tiempo real
const productosFiltrados = computed(() =>
  productos.value.filter(p =>
    p.nombre.toLowerCase().includes(busqueda.value.toLowerCase())
  )
)

onMounted(async () => {
  try {
    const respuesta = await axios.get('http://localhost:8000/api/productos')
    productos.value = respuesta.data
  } catch (error) {
    console.error('Error al cargar productos:', error)
  }
})
</script>