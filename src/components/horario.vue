<template>
    <div class="container">
        <h3>Horario de Clases - 6to Semestre Ingeniería en Sistemas</h3>
        <table class="table">
            <thead>
                <tr>
                    <th scope="col">MATERIA</th>
                    <th scope="col">DOCENTE (RFC)</th>
                    <th scope="col">LUNES</th>
                    <th scope="col">MARTES</th>
                    <th scope="col">MIÉRCOLES</th>
                    <th scope="col">JUEVES</th>
                    <th scope="col">VIERNES</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(row, index) in Horario" :key="index">
                    <td class="materia">{{ row.materia }}</td>
                    <td class="docente">{{ row.docente }}<br><small>{{ row.rfc }}</small></td>
                    <td>{{ row.lunes }}</td>
                    <td>{{ row.martes }}</td>
                    <td>{{ row.miercoles }}</td>
                    <td>{{ row.jueves }}</td>
                    <td>{{ row.viernes }}</td>
                </tr>
            </tbody>
        </table>
    </div>
    </template>
    
    <script setup>
    import { ref } from 'vue'
    
    const Horario = ref([
    {
        materia: 'SCD1015/6AS/LENGUAJES Y AUTOMATAS 1',
        docente: 'ACEVEDO BAUTISTA IVOR',
        lunes: '',
        martes: '12:00-14:00/ACS',
        miercoles: '',
        jueves: '11:00-13:00/ACS',
        viernes: '12:00-13:00/ACS'
    },
    {
        materia: 'SCD1021/6AS/REDES DE COMPUTADORAS',
        docente: 'GARCIA HERNANDEZ ASTRID MILDRED',
        lunes: '11:00-13:00/RDS',
        martes: '',
        miercoles: '11:00-13:00/RDS',
        jueves: '',
        viernes: '13:00-14:00/RDS'
    },
    {
        materia: 'AEB1055/6AS/PROGRAMACION WEB',
        docente: 'JOSUE VASQUEZ',
        lunes: '15:00-17:00/ACS',
        martes: '',
        miercoles: '13:00-15:00/RDS',
        jueves: '',
        viernes: '15:00-16:00/LDS'
    },
    {
        materia: 'SCA1026/6AS/TALLER DE SISTEMAS OPERATIVOS',
        docente: 'CRUZ PEREZ JORGE',
        lunes: '',
        martes: '15:00-17:00/ACS',
        miercoles: '',
        jueves: '15:00-17:00/ACS',
        viernes: ''
    },
    {
        materia: 'SCB1001/6AS/ADMINISTRACION DE BASE DE DATOS',
        docente: 'SOLANO HERNANDEZ MIGUEL',
        lunes: '17:00-19:00/RDS',
        martes: '',
        miercoles: '13:00-15:00/RDS',
        jueves: '',
        viernes: '16:00-17:00/RDS'
    },
    {
        materia: 'SCC1014/6AS/LENGUAJES DE INTERFAZ',
        docente: 'SANCHEZ VASQUEZ LUCIA',
        lunes: '',
        martes: '17:00-19:00/LDS',
        miercoles: '',
        jueves: '17:00-19:00/LDS',
        viernes: ''
    },
    {
        materia: 'SCD1011/6AS/INGENIERIA DE SOFTWARE',
        docente: 'ROMAN CRUZ JOSE ALFREDO',
        lunes: '13:00-15:00/RDS',
        martes: '',
        miercoles: '15:00-17:00/RDS',
        jueves: '',
        viernes: '14:00-15:00/RDS'
    }
    ])
    </script>
    
    <style scoped>
    .container {
      margin: 30px auto;
      padding: 30px;
      
      border-radius: 18px;
      
      max-width: 1100px;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
    
    h3 {
      text-align: center;
      font-size: 28px;
      color: white;
      background: linear-gradient(135deg, #1a237e, #283593);
      padding: 15px;
      border-radius: 12px;
      margin: -15px -15px 30px -15px;
      font-weight: 600;
    }
    
    .table {
      width: 100%;
      border-spacing: 0;
      text-align: center;
      
      
    }
    
    .table th {
      background: linear-gradient(to right, #1a237e, #3949ab);
      color: white;
      font-size: 16px;
      padding: 16px;
      font-weight: 500;
    }
    
    
    
    .table td {
      font-size: 15px;
      color: #333;
      background-color: #f5f5f5;
      padding: 14px;
      border-bottom: 1px solid #e0e0e0;
      
    }
    
    
    
    </style>