<script setup>
const nombre = 'Juanan';
const colorDeEstilo = 'color: blue';
const arrayColores = ['blue', 'green', 'peru'];
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
</template>

<style>
h1 {
  color: red;
}
</style>
