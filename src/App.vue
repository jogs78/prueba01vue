<script setup>
import Formulario from './Formulario.vue'
import { ref } from 'vue'
const activo = ref(false)

</script>

<template>
    Formulario para sacar un correo:
    <Formulario />
    Formulario para sacar una beca:
    <Formulario />
    Formulario para otra cosa:
    <Formulario />
    Formulario en el App:
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
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
