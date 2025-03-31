<script setup>
import { ref } from 'vue'
import Hijo11 from './Hijo1-1.vue';
import Hijo22 from './Hijo2-2.vue';
</script>
<template>  
<div class="container">
    <div class="row">
                <div class="col-md-4">
                    <div class="card mt-4">
                        <div style="background-color:#a3e4d7;" class="card-header">
                            <h1 class="estilo">        Soy el componente Padre 
                            </h1>
                        </div>
                        <div class="card-body">
                            <P class="parrafo">Los props son atributos personalizados que se usan en Vue para pasar datos entre componentes.</P>
                            <img class="img" src="/src/assets/ImgProps/Padre.png" alt="FRACTAL">
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="card mt-4">
                        <div style="background-color: #a3e4d7;" class="card-header">
                            <h1 class="estilo">   HIJO 1     
                            </h1>
                        </div>
                        <div class="card-body">
                            <Hijo11 class="mt-4 parrafo" descripcion="Características de los props: " />
                            <Hijo11 class="mt-4 parrafo" descripcion="♠ Son una opción de configuración en Vue " />
                            <Hijo11 class="mt-4 parrafo" descripcion="♠ Son de solo lectura y no pueden ser modificados por el componente secundario " />
                            <Hijo11 class="mt-4 parrafo" descripcion="♠ Permiten crear componentes reutilizables y modulares " />
                            <Hijo11 class="mt-4 parrafo" descripcion="♠ Son esenciales para la comunicación entre componentes " />
                            <img class="img" src="/src/assets/ImgProps/Hijo1.png" alt="">
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="card mt-4">
                        <div style="background-color: #a3e4d7" class="card-header">
                            <h1 class="estilo">HIJO 2</h1>
                        </div>
                        <div class="card-body">
                            <Hijo22 class="mt-4 parrafo" descripcion="Cómo usar los props:" />
                            <Hijo22 class="mt-4 parrafo" descripcion="• Se pueden pasar a los componentes a través de atributos personalizados a la etiqueta del componente " />
                            <Hijo22 class="mt-4 parrafo" descripcion="• Se pueden validar y manipular los datos recibidos como props antes de utilizarlos " />
                            <Hijo22 class="mt-4 parrafo" descripcion="• Se pueden pasar props a una ruta cualquiera siempre y cuando estén activados " />
                            <img class="img" width="270" height="200" src="/src/assets/ImgProps/Hijo2.png" alt="">

                        </div>
                    </div>
                </div>
                    </div>  
</div>
</template>

<style scoped>
.parrafo{
    text-align: center;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}
.estilo{
    text-align: center;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
}
.img{
    border-radius: 20px;
  width: 300px; 
  height: auto; 
  box-shadow: 5px 5px 15px rgba(24, 23, 23, 0.6);
  margin-left: 50px;
}
</style>
