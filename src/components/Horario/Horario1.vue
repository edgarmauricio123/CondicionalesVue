<script setup>
import { ref } from 'vue';
const Horario = ref([
    { materia: 'SCD1015/6BS/LENGUAJES Y AUTOMATAS I SOLANO HERNANDEZ MIGUEL ANGEL ', rep:'N',cr:'S',lunes:'11:00-13:00/MAGS',Martes:'',Miercoles:'11:00-13:00/4',Jueves:'',Viernes:'12:00-13:00/RDS',Sabado:'',Domingo:''},
    { materia: 'SCD1021/6BS/REDES DE COMPUTADORAS SANCHEZ VASQUEZ LUCIA ',rep:'N',cr:'S',lunes:'',Martes:'13:00-15:00/RDS',Miercoles:'',Jueves:'13:00-15:00/LDS',Viernes:'16:00-17:00/LDS',Sabado:'',Domingo:''},
    { materia: 'AEB1055/6BS/PROGRAMACION WEB null  ', rep: 'N',cr:'S', lunes:'',Martes: '', Miercoles: '', Jueves: '17:00-19:00/ACS ', Viernes: '13:00-14:00/ACS ',Sabado:'',Domingo:'' },
    { materia: 'SCA1026/6BS/TALLER DE SISTEMAS OPERATIVOS CRUZ PEREZ JORGE  ', rep: 'N',cr:'S',lunes:'13:00-15:00/LDS ', Martes: '', Miercoles: '13:00-15:00/LDS ', Jueves: '', Viernes: '',Sabado:'',Domingo:'' },
    { materia: 'SCB1001/6BS/ADMINISTRACION DE BASES DE DATOS GARCIA HERNANDEZ HILARIO VIDAL  ', rep: 'N',cr:'S',lunes:'', Martes: '15:00-17:00/MAG 4 ', Miercoles: '15:00-17:00/LDS ', Jueves: '', Viernes: '14:00-18:00/LDS ',Sabado:'',Domingo:'' },
    { materia: 'SCC1014/685/LENGUAJES DE INTERFAZ SANCHEZ VASQUEZ LUCIA   ', rep: 'N',cr:'S',lunes:'', Martes: '11:00-13:00/MAG 2 ', Miercoles: '17:00-19:00/RDS ', Jueves: '', Viernes: '',Sabado:'',Domingo:'' },
    { materia: 'SCD1011/68S/INGENIERIA DE SOFTWARE ROMAN CRUZ JOSE ALFREDO   ', rep: 'N',cr:'S',lunes:'5 15:00-17:00/LDS ', Martes: '', Miercoles: '', Jueves: '15:00-17:00/LDS ', Viernes: '15:00-16:00/RDS',Sabado:'',Domingo:'' },
])
const informacion = ref([
    { nc: '22620066', nombre: 'Sarmiento Ruiz Edgar Mauiricio', Grado: '6', Periodo: 'ENE-JUN 25' },
])
const carrera = ref([
    { carrerara: 'INGENIERIA EN SISTEMAS COMPUTACIONALES', especialidad: '         ', Créditos: '13', Plan: 'ISIC-2010-2024' },
])
</script>
<template>
    <div class="container">
        <div class="container">
            <h1>Carga Academica</h1>
            <table class="table table-bordered">
                <thead class="table-active">
                    <tr >
                        <th scope="col">N° control</th>
                        <th scope="col">Nombre</th>
                        <th scope="col">Grado</th>
                        <th scope="col">Periodo</th>
                    </tr>
                </thead>
                <tbody class="table-group-divider">
                    <tr v-for="(row, index) in informacion" :key="index">
                        <td>{{ row.nc }}</td>
                        <td>{{ row.nombre }}</td>
                        <td>{{ row.Grado }}</td>
                        <td>{{ row.Periodo }}</td>
                    </tr>
                </tbody>
            </table>
        </div>
        </div>
        <div class="container">
        <div class="container">
            <table class="table table-bordered">
                <thead class="table-active" >
                    <tr >
                        <th scope="col">Carrera</th>
                        <th scope="col">Especialidad</th>
                        <th scope="col">Creditos</th>
                        <th scope="col">Plan de Estudios</th>
                    </tr>
                </thead>
                <tbody class="table-group-divider">
                    <tr v-for="(row, index) in carrera" :key="index">
                        <td>{{ row.carrerara }}</td>
                        <td>{{ row.especialidad }}</td>
                        <td>{{ row.Créditos }}</td>
                        <td>{{ row.Plan }}</td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="container">
            <h3 class="titulo">HORARIO DE CLASES DE SISTEMAS</h3>
            <table class="table table-bordered">
                <thead>
                    <tr class="table-active">
                        <th scope="col">Materia</th>
                        <th scope="col">Rep</th>
                        <th scope="col">Cr</th>
                        <th scope="col">Lunes</th>
                        <th scope="col">Martes</th>
                        <th scope="col">Miercoles</th>
                        <th scope="col">Jueves</th>
                        <th scope="col">Viernes</th>
                        <th scope="col">Sabado</th>
                        <th scope="col">Domingo</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(row, index) in Horario" :key="index">
                        <td>{{ row.materia }}</td>
                        <td>{{ row.rep }}</td>
                        <td>{{ row.cr }}</td>
                        <td>{{ row.lunes }}</td>
                        <td>{{ row.Martes }}</td>
                        <td>{{ row.Miercoles }}</td>
                        <td>{{ row.Jueves }}</td>
                        <td>{{ row.Viernes }}</td>
                        <td>{{ row.Sabado }}</td>
                        <td>{{ row.Domingo }}</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
<br><br><br><br><br>
</template>
<style>
h1{
    text-align: center;
    font-family: Georgia, 'Times New Roman', Times, serif;
}

.titulo{
    color: black;
    background-color: rgb(192, 180, 189);
    border-radius: 0%;
    padding: 10px;
}
</style>