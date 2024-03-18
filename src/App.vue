<script setup>
const nombre = 'Juanan';
const colorDeEstilo = 'color: blue';

console.log('Hola Vue');
</script>

<template>
  <h1>Hola Vue</h1>
  <h1>Hola {{ nombre || 'valor por defecto' }}</h1>
  <h1 v-bind:style="colorDeEstilo">Hola Azul</h1>
  <h1 :style="colorDeEstilo">Hola Azul también</h1>
</template>

<style>
h1 {
  color: red;
}
</style>
