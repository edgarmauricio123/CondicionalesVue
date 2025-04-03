<script>
export default {
    data() {
        return {
            numero1: 0,
            numero2: 0,
            resultado: 0,
        }
    },
    methods: {
        sumar() {
            this.resultado = parseFloat(this.numero1) + parseFloat(this.numero2);
        },
        resta() {
            this.resultado = parseFloat(this.numero1) - parseFloat(this.numero2);
        },
        multiplicar() {
            this.resultado = parseFloat(this.numero1) * parseFloat(this.numero2);
        },
        dividir() {
            this.resultado = parseFloat(this.numero1) / parseFloat(this.numero2);
        }
    }
}

</script>
<template>
    <div class="container mt-5">
        <div class="card shadow p-4">
            <h1 class="text-center">Calculadora V1</h1>

            <div class="input-group input-group-sm mb-3">
                <span class="input-group-text" id="inputGroup-sizing-sm">Resultado:</span>
                <input type="text" class="form-control" aria-label="Sizing example input"
                    aria-describedby="inputGroup-sizing-sm" v-model="resultado">
            </div>
            <div class="mb-3">
                <label for="">Numero 1</label>
                <input type="number" class="form-control" v-model="numero1">
            </div>
            <div class="mb-3">
                <label for="">Numero 2</label>
                <input type="number" class="form-control" v-model="numero2">
            </div>
            <div class="d-flex justify-content-center gap-2">
                <button @click="sumar" class="btn btn-danger gap-2">sumar</button>
                <button @click="resta" class="btn btn-warning gap-2">Resta</button>
                <button @click="multiplicar" class="btn btn-warning gap-2">Multiplicar</button>
                <button @click="dividir" class="btn btn-warning gap-2">Dividir</button>
            </div>

        </div>


    </div>
</template>
