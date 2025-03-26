<script setup>
import { ref } from 'vue'

const bienvenida = ref("Bienvenidos a la sección de condicionales")
const  nombre = ref("Edgar mauricio")
const apellidos = ref("Sarmiento Ruiz")

// defineProps({
//   msg: String,
// })

</script>

<template>
  <div class="container">
    <h2 class="text-center">{{ bienvenida }}</h2>
    <div class="row">
      <div class="cold-md-6">
        <h6 class="">{{ nombre }}</h6>
        <h6>{{ apellidos }}</h6>
      </div>
    </div>


  </div>

</template>

<style scoped>

</style>
