<script setup>
import { ref } from 'vue';

const Horario = ref([
    {hora:'07:00 - 09:00 ', Lunes: 'IA',  Martes: 'Agil',  Miercoles: 'Web', Jueves: 'Ia', Viernes: 'Movil'},
    {hora:'09:00 - 11:00 ', Lunes: 'IA',  Martes: 'Agil',  Miercoles: 'Web', Jueves: 'Ia', Viernes: 'Movil'},
    {hora:'11:00 - 13:00 ', Lunes: 'Libre',  Martes: 'Agil',  Miercoles: 'Web', Jueves: 'Ia', Viernes: 'Movil'},
    {hora:'13:00 - 15:00 ', Lunes: 'IA',  Martes: 'Agil',  Miercoles: 'Web', Jueves: 'Ia', Viernes: 'Movil'},
    {hora:'15:00 - 17:00 ', Lunes: 'IA',  Martes: 'Agil',  Miercoles: 'Web', Jueves: 'Ia', Viernes: 'Movil'}

 
])
</script>

<template>
    <div class="container">
        <h3>HORARIO DE CLASES DE SISTEMAS</h3>
        <table class="table ">
  <thead>
    <tr>
      <th scope="col">Hora</th>
      <th scope="col">Lunes</th>
      <th scope="col">Martes</th>
      <th scope="col">Miercoles</th>
      <th scope="col">Jueves</th>
      <th scope="col">Viernes</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="(row, index) in Horario" :key="index">
        <td>{{ row.hora }}</td>
        <td>{{ row.Lunes }}</td>
        <td>{{ row.Martes }}</td>
        <td>{{ row.Miercoles }}</td>
        <td>{{ row.Jueves }}</td>
        <td>{{ row.Viernes }}</td>
    </tr>


  </tbody>
</table>

    </div>


</template>

<style>

</style>