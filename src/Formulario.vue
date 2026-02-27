<script setup>
import { ref } from 'vue'
const activo = ref(false)
</script>

<template>
    <form action="">
      <label for='nombre'>nombre</label>
      <input type='text' name='nombre' id='nombre'><br>
      <label for='apellido'>apellido</label>
      <input type='text' name='apellido' id='apellido'><br>
      <label for='estudia'>estudia</label>
      <input type="checkbox" v-model="activo"> 

      <span v-if="activo == true">
       <label for='escuela'>escuela</label>
        <select name="escuela" id="escuela">
          <option value="01">Tecnologico</option>
          <option value="02">Unach</option>
          <option value="03">Otra</option>
        </select>
      </span>

      <input type="submit" value="Registrar">
 
 
    </form>
    
</template>

<style scoped>
  form {
    border: 2px solid black; 
  }
</style>
