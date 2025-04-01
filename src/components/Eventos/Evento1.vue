<template>
    <div class="container">
        <div class="row mt-4">
            <div>
                <h4 class="txt">Ejemplo formulario</h4>
                <label class="input-group-text" for="nombre">Ingresa tu nombre</label>
                <input class="form-control mt-2" type="text" id="nombre" v-model="nombre">
                <button @click="soyButton" class="btn btn-warning mt-3 mx-2" type="button">Guardar</button>
                <p class="mt-2">El nombre ingresado es: <strong>{{ actualizar }}</strong></p>
            </div>

            <div>
                <h3 class="txt">Ejemplo de mouseenter y mouseleave</h3>
                <p class="txt">Pase el mouse</p>   
                <p class="txt">{{ mensaje }}</p>

                <div class="contenedor-img" @mouseenter="mostrarMensaje" @mouseleave="ocultarMensaje">
                    <img class="imagen" src="https://thumbs.dreamstime.com/b/autob%C3%BAs-retro-del-viaje-con-el-fondo-del-vintage-34993958.jpg" alt="Autobús retro">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            nombre: '',
            mensaje: '',
            actualizar: ''
        }
    },
    methods: { 
        soyButton() {
            this.actualizar = this.nombre; // Al hacer clic, guarda el nombre en "actualizar"
        },
        mostrarMensaje() {
            this.mensaje = "El mouse está dentro del rectángulo";
        },
        ocultarMensaje() {
            this.mensaje = "El mouse está fuera del rectángulo";
        }
    }
}
</script>

<style>
.txt {
    text-align: center;
    font-family: cursive;
}

.contenedor-img {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 15px;
}

.imagen {
    border-radius: 14px;
    max-width: 100%;
    height: auto;
}
</style>
