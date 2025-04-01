<script>
export default{
    data(){
        return{
            numero1: 0,
            numero2: 0,
            resultado: 0,
            operacionSeleccionada: null
        }
    },
    methods:{
        sumar(){
            this.resultado = parseFloat(this.numero1) + parseFloat(this.numero2);
            this.operacionSeleccionada = 'sumar';
        },
        resta(){
            this.resultado = parseFloat(this.numero1) - parseFloat(this.numero2);
            this.operacionSeleccionada = 'resta';
        },
        multiplicar(){
            this.resultado = parseFloat(this.numero1) * parseFloat(this.numero2);
            this.operacionSeleccionada = 'multiplicar';
        },
        dividir(){
            this.resultado = parseFloat(this.numero1) / parseFloat(this.numero2);
            this.operacionSeleccionada = 'dividir';
        }
    }
}
</script>
<template>
    <div class="container mt-5">
        <div class="card shadow p-4">
            <h1 class="text-center">Calcuflex</h1>
            <h2 class="text-center mt-4">R = {{ resultado }}</h2>

            <div class="d-flex">
                <div class="flex-grow-1">
                    <div class="mb-3">
                        <input type="Number" class="form-control" v-model="numero1">
                    </div>
                    <div class="mb-3">
                        <input type="Number" class="form-control" v-model="numero2">
                    </div>
                </div>
                
                <div class="d-flex flex-column ms-2 gap-2">
                    <button @click="sumar" 
                            class="btn" 
                            :class="{'btn-success': operacionSeleccionada === 'sumar', 'btn-warning': operacionSeleccionada !== 'sumar'}">+</button>
                    <button @click="resta" 
                            class="btn" 
                            :class="{'btn-success': operacionSeleccionada === 'resta', 'btn-warning': operacionSeleccionada !== 'resta'}">-</button>
                    <button @click="multiplicar" 
                            class="btn" 
                            :class="{'btn-success': operacionSeleccionada === 'multiplicar', 'btn-warning': operacionSeleccionada !== 'multiplicar'}">*</button>
                    <button @click="dividir" 
                            class="btn" 
                            :class="{'btn-success': operacionSeleccionada === 'dividir', 'btn-warning': operacionSeleccionada !== 'dividir'}">/</button>
                </div>
            </div>
        </div>
    </div>
</template>

<style>
h1{
    color: #797070;
    padding: 5px;
    text-align: center;
}

.card{
    background-color: rgb(255, 255, 255);
    border-radius: 20px;
    width: 300px;
    margin: auto;
}

h2{
    color: rgb(255, 255, 255);
    background-color: rgba(216, 46, 33, 0.5);
    padding: 5px;
    border-radius: 15px;
}
</style>