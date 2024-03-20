<script setup>
const nombre = 'Juanan';
const colorDeEstilo = 'color: blue';
const arrayColores = ['blue', 'green', 'peru'];
const arrayFrutas = ['🍎', '🍌', '🍉', '🍓', '🍒'];

const activo = true;

console.log('Hola Vue');
</script>

<template>
  <h1>Hola Vue</h1>
  <h1>Hola {{ nombre.toUpperCase() || 'valor por defecto' }}</h1>
  <h1 v-bind:style="colorDeEstilo">Hola Azul</h1>
  <h1 :style="colorDeEstilo">Hola Azul también</h1>

  <h2>Esto se interpreta como texto: {{ arrayColores }}</h2>
  <h2 :style="`color: ${arrayColores[2]}`">Hola array de colores</h2>
  <h2>
    {{ activo ? 'Estoy activo' : 'Estoy inactivo' }}
  </h2>

  <h2 v-if="activo">Si me ves, es que mi condicion es activo</h2>
  <h2 v-else="!activo">Si me ves, es que mi condicion es inactivo</h2>
  <h2 v-if="!activo">Si me ves, es que mi condicion es inactivo</h2>

  <h2 v-if="activo">Si me ves, es que estoy activo y estoy probando elseif</h2>
  <h2 v-else-if="activo === false">Si me ves, es que estoy inactivo</h2>
  <h2 v-else>Si me ves, es que estoy indeciso y mi condicion es NULL, CERO o ESPACIO VACÍO</h2>

  <!-- V-SHOW cambia la propiedad DISPLAY a NONE -->
  <h2 v-show="activo">Si me ves, es que mi condicion es V-SHOW = TRUE</h2>

  <!-- V-FOR es similar a los map() o forEach() de ReactJS -->
  <ul>
    <li v-for="fruta in arrayFrutas">{{ fruta }}</li>
  </ul>
</template>

<style>
h1 {
  color: red;
}
</style>
