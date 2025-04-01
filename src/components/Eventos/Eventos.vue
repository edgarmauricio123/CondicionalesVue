<template >
   <div class="container">
    <div class="row mt-4">
        <div>
            <h4>Evento Click</h4>
            <button @click="click" class="btn btn-danger" type="button">Dale clic</button>
            <button @click="soyButton" class="btn btn-warning mx-2" type="button">Dale clic 2</button>
        </div>
        <div>
            <h4>Evento change</h4>
            <label class="input-group-text" for="">Ingresa tu nombre</label>
            <input class="form-control mt-2" type="text" id="nombre" @change="nombreE">
            <p>El nombre ingresado es: <strong>{{ nombre }}</strong></p>
        </div>

        <div>
            <h3>Evento de mouseenter y mouseleave</h3>
        <div  class="text-center"
         style="color: white; width: 300px; height: 200px; background-color: black;text-align: center;padding: 15px;border-radius: 14px;"
          @mouseenter="mostrarMensaje" @mouseleave="ocultarMensaje">
         <p>Pase el mouse</p>   
         <p>{{ mensaje }}</p>

        </div>
        </div>
    </div>
   </div>
</template>
<script>
export default {
    data() {
        return {
            nombre:'',
            mensaje:'',
        }
    },
   methods:{ 
    nombreE(event){
        this.nombre = event.target.value
    },
    click() {
        alert("Gracias por darle clic")
    },
    soyButton(){
        alert("Soy un boton")
    },
   
    mostrarMensaje(){
        this.mensaje="El mouse esta dentro del rectangulo"
    },
    ocultarMensaje(){
        this.mensaje="El mouse esta fuera del rectangulo"
    },
   }
}
</script>
<style >
    
</style>