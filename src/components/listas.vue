<script>
export default {
  data() {
    return {
      alumnos: [
        { numc: 22621001, nombre: "Ana Lucía Mendoza Ríos", carrera: "ISC", Hobie: "Programar apps" },
        { numc: 22621002, nombre: "Diego Armando Flores Castro", carrera: "IC", Hobie: "Robótica" },
        { numc: 22621003, nombre: "Valeria Sánchez Ortiz", carrera: "IGE", Hobie: "Viajar" },
        { numc: 22621004, nombre: "Jorge Eduardo Ramírez Vega", carrera: "ISC", Hobie: "Ciberseguridad" },
        { numc: 22621005, nombre: "Adriana Martínez Pineda", carrera: "IC", Hobie: "Astronomía" },
        { numc: 22621006, nombre: "Oscar Daniel Herrera Luna", carrera: "IGE", Hobie: "Fotografía" },
        { numc: 22621007, nombre: "Lucía Fernanda Vargas Díaz", carrera: "ISC", Hobie: "Inteligencia Artificial" },
        { numc: 22621008, nombre: "Ricardo González Méndez", carrera: "IC", Hobie: "Drones" },
        { numc: 22621009, nombre: "Gabriela Soto Navarro", carrera: "IGE", Hobie: "Negocios digitales" },
        { numc: 22621010, nombre: "Juan Pablo Reyes Ortega", carrera: "ISC", Hobie: "Videojuegos" }
      ]
    }
  }
}
</script>

<template>
  <div class="container">
    <h3 class="title">Lista de Alumnos</h3>
    <ul class="student-list">
      <li v-for="alumno in alumnos" :key="alumno.numc" class="student-card">
        <p><span class="label">N_Control:</span> {{ alumno.numc }}</p>
        <p><span class="label">Nombre:</span> {{ alumno.nombre }}</p>
        <p><span class="label">Carrera:</span> {{ alumno.carrera }}</p>
        <p><span class="label">Hobie:</span> {{ alumno.Hobie }}</p>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  font-family: Arial, sans-serif;
}

.title {
  color: #2c3e50;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  text-align: center;
  
}

.student-list {
  list-style: none;
  padding: 0;
  display: grid;
  gap: 15px;
}

.student-card {
  background-color: #338feb;
  color: black;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 15px;
  border-radius: 8px;
  padding: 15px;
  text-align: left;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.student-card:hover {
  background-color: #004181;
}

.label {
  font-weight: bold;
  color: #ffffff;
  display: inline-block;
  width: 80px;
}

p {
  margin: 5px 0;
}
</style>