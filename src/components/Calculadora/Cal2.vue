<script>
export default {
  data() {
    return {
      display: '',
      currentValue: 0,
    };
  },
  methods: {
    agregarNumero(numero) {
      this.display += numero;
    },
   
    calculo() {
      try {
        this.currentValue = eval(this.display);
        this.display = this.currentValue.toString();
      } catch (error) {
        this.display = "Error";
      }
    },
    Limpiardisplay() {
      this.display = '';
    },
    EliminarNumero() {
      this.display = this.display.slice(0, -1);
    },
    calcularPorcentaje() {
      if (this.display !== '' && !isNaN(this.display)) {
        this.display = (parseFloat(this.display) / 100).toString();
      }
    }
  }
};
</script>

<template>
  <div class="container d-flex justify-content-center align-items-center" style="min-height: 100vh; background-color:white;">
    <div class="card p-3" style="width: 320px; background-color: #ffffff; border-radius: 15px; box-shadow: 0 10px 25px rgba(0, 0, 0, 0.8); border: none;">
      <div class="card-body">
        <h6 class="text-center mb-3" style="color: #5d5d5d; font-weight: 600;">Calculadora V2</h6>

        <!-- Display de la calculadora -->
        <div class="mb-4">
          <input type="text" class="form-control text-end fs-4" v-model="display" disabled 
                 style="background-color: #f8f9fa; border: 2px solid #e9ecef; height: 60px; border-radius: 10px; color: #333; font-weight: 500;">
        </div>
        
        <!-- Botones de la calculadora -->
        <div class="d-flex justify-content-between gap-2 mb-2">
          <button class="btn btn-light flex-fill" @click="calcularPorcentaje()" style="border-radius: 8px; font-weight: 500; color: #5d5d5d; border: 1px solid #e0e0e0;">%</button>
          <button class="btn btn-light flex-fill" @click="Limpiardisplay()" style="border-radius: 8px; font-weight: 500; color: #5d5d5d; border: 1px solid #e0e0e0;">CE</button>
          <button class="btn btn-light flex-fill" @click="Limpiardisplay()" style="border-radius: 8px; font-weight: 500; color: #5d5d5d; border: 1px solid #e0e0e0;">C</button>
          <button class="btn flex-fill" @click="EliminarNumero()" style="border-radius: 8px; font-weight: 500; background-color: #ff6b6b; color: white; border: none;">⌫</button>
        </div>

        <div class="d-flex justify-content-between gap-2 mb-2">
          <button class="btn btn-light flex-fill" @click="agregarNumero(7)" style="border-radius: 8px; font-weight: 500; color: #333; border: 1px solid #e0e0e0;">7</button>
          <button class="btn btn-light flex-fill" @click="agregarNumero(8)" style="border-radius: 8px; font-weight: 500; color: #333; border: 1px solid #e0e0e0;">8</button>
          <button class="btn btn-light flex-fill" @click="agregarNumero(9)" style="border-radius: 8px; font-weight: 500; color: #333; border: 1px solid #e0e0e0;">9</button>
          <button class="btn flex-fill" @click="agregarNumero('/')" style="border-radius: 8px; font-weight: 500; background-color: #4dabf7; color: white; border: none;">/</button>
        </div>

        <div class="d-flex justify-content-between gap-2 mb-2">
          <button class="btn btn-light flex-fill" @click="agregarNumero(4)" style="border-radius: 8px; font-weight: 500; color: #333; border: 1px solid #e0e0e0;">4</button>
          <button class="btn btn-light flex-fill" @click="agregarNumero(5)" style="border-radius: 8px; font-weight: 500; color: #333; border: 1px solid #e0e0e0;">5</button>
          <button class="btn btn-light flex-fill" @click="agregarNumero(6)" style="border-radius: 8px; font-weight: 500; color: #333; border: 1px solid #e0e0e0;">6</button>
          <button class="btn flex-fill" @click="agregarNumero('*')" style="border-radius: 8px; font-weight: 500; background-color: #4dabf7; color: white; border: none;">×</button>
        </div>

        <div class="d-flex justify-content-between gap-2 mb-2">
          <button class="btn btn-light flex-fill" @click="agregarNumero(1)" style="border-radius: 8px; font-weight: 500; color: #333; border: 1px solid #e0e0e0;">1</button>
          <button class="btn btn-light flex-fill" @click="agregarNumero(2)" style="border-radius: 8px; font-weight: 500; color: #333; border: 1px solid #e0e0e0;">2</button>
          <button class="btn btn-light flex-fill" @click="agregarNumero(3)" style="border-radius: 8px; font-weight: 500; color: #333; border: 1px solid #e0e0e0;">3</button>
          <button class="btn flex-fill" @click="agregarNumero('-')" style="border-radius: 8px; font-weight: 500; background-color: #4dabf7; color: white; border: none;">-</button>
        </div>

        <div class="d-flex justify-content-between gap-2">
          <button class="btn flex-fill" @click="calculo()" style="border-radius: 8px; font-weight: 500; background-color: #40c057; color: white; border: none; height: 50px;">=</button>
          <button class="btn btn-light flex-fill" @click="agregarNumero(0)" style="border-radius: 8px; font-weight: 500; color: #333; border: 1px solid #e0e0e0;">0</button>
          <button class="btn btn-light flex-fill" @click="agregarNumero('.')" style="border-radius: 8px; font-weight: 500; color: #333; border: 1px solid #e0e0e0;">.</button>
          <button class="btn flex-fill" @click="agregarNumero('+')" style="border-radius: 8px; font-weight: 500; background-color: #4dabf7; color: white; border: none;">+</button>
        </div>
      </div>
    </div>
  </div>
</template>