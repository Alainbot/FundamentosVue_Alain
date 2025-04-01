<template>
  <div class="container">
    <div class="row">
      <div class="section">
        <h4>Evento click</h4>
        <div class="button-group">
          <button @click="clic" class="btn btn-danger">Dale click</button>
          <button @click="soyBoton" class="btn btn-warning">Dale click 2</button>
        </div>
      </div>
      
      <div class="section">
        <h4>Evento Changee</h4>
        <div class="input-group">
          <label>Ingresa tu nombre>></label>
          <input type="text" id="nombre" class="form-input" @change="nombreE">
          <p class="result" >El nombre ingresado es: <strong>{{ nombre }}</strong></p>
        </div>
      </div>
      
      <div class="section">
        <h4>Evento de mouseenter y mouseleave</h4>
        <div class="hover-box" @mouseenter="mostrarMensaje" @mouseleave="ocultarMensaje">
          <p>Pase el mouse</p>     
          <p>{{ mensaje }}</p>           
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
 
  font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.section {
  background-image: url(https://i.blogs.es/bb4027/neon/1366_2000.jpeg);
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.7);
}

h4 {
  margin-top: 0;
  color: #252425;
  font-size: 20px;
}

.button-group {
  display: flex;
  justify-content:center ;
  gap: 100px;
  margin-top: 10px;
}

.btn {
  padding: 8px 16px;
  border: none;
  border-radius: 40%;
  cursor: pointer;
  font-weight: 500;
  transition: all 0.2s;
}

.btn:hover {
  transform: translateY(-1px);
}

.btn-danger {
  background: #35dc43;
  color: white;
}

.btn-warning {
  background: #33b6bb;
  color: #fafcfd;
}

.input-group {
  width: 100%;
  max-width: 600px;
  padding: 8px 22px;
  border-radius: 4px;
  color: #000000;
 
}

label {
  display: block;
  margin-right: 10px;
  margin-bottom: 10px;
    
}

.form-input {
  width: 100%;
  max-width: 300px;
  padding: 8px 22px;
  border-radius: 4px;
  color: #2c201f;
  background-color: #f8f9fa;
}

.result {
  
  margin-top: 10px;
  color: #aaa8a8;
}

.hover-box {
  width: 300px;
  height: 200px;
  background: #165083;
  color: rgb(185, 173, 173);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 15px;
  margin-top: 10px;
  cursor: pointer;
  transition: background 0.3s;
}

.hover-box:hover {
  background: #165083;
}
</style>

<script>
export default {
  data(){
    return{
      nombre: "",
      mensaje: ""
    }
  },
  methods:{
    clic(){
      alert("Hola mundo")
    },
    soyBoton(){
      alert("Soy el boton 2")
    },
    nombreE(event){
      this.nombre = event.target.value
      console.log(this.nombre)
    },
    mostrarMensaje(){
      this.mensaje = "El mouse está sobre el rectángulo"
    },
    ocultarMensaje(){
      this.mensaje = "El mouse está fuera del rectángulo"
    }
  }
}
</script>