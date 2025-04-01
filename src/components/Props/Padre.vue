<script setup>
import {ref} from 'vue'
import Hijo1 from './Hijo.vue'  
import Hijo2 from './Hijo2.vue'  

defineProps({
   msg: String,
})
</script>

<template>
  <div class="container">
    <h1>Soy el componente padre</h1>

    <Hijo1 class="mt-4" edad="10"/>
    <Hijo2 class="mt-4" edad="4"/>
  </div>
</template>

<style scoped>
.container {
  max-width: 800px;
  padding: 2rem;
  text-align: center;
  font-family: 'Arial', sans-serif;
  color: #2c3e50;
  background-color: #ffffffa8;
  border-radius: 8px;
  box-shadow: 2px 4px 6px rgba(0, 0, 0, 0.5);
}

h1 {
  color: #000000;
 
  padding-bottom: 0.5rem;
}

</style>