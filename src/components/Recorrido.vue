<script>
export default{

    data(){
        return{
            // DATOS DE ALUMNOS 

            alumnos:[
                {nc:12345, nombre:'Edgar', carrerar:'ISC' },
                {nc:12345, nombre:'Pedro', carrerar:'Industrial' },
                {nc:12345, nombre:'Marco', carrerar:'Civil' }

            ]
        }
    }
}

</script>
<template>
<div class="container">
    <h3 class="mt-4 , text-center">Lista de alumnos</h3>
    <ul>
        <li v-for="alumno in alumnos" :key="alumno.nc">
            <strong>{{ alumno.nombre }} </strong> -
            <strong>{{ alumno.carrerar }}</strong>

        </li>
    </ul>
</div>

</template>
<style>
h3 {
    color: black;
    background-color: rgb(220, 131, 198);
    border-radius: 15px;
    padding: 10px;
}
ul{
    color: blueviolet;
    /* esto es para que no se vean los puntitos */
    list-style-type: none;  
    padding: 0%;
}

li{

    color: white;
    background-color: black;
    border-radius: 15px;
    padding: 10px;
    margin: 10px;
    text-align: start;
}

</style>