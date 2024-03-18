<script setup>
const nombre = 'Juanan';
console.log('Hola Vue');
</script>

<template>
  <h1>Hola Vue</h1>
  <h1>Hola {{ nombre || 'valor por defecto' }}</h1>
</template>

<style>
h1 {
  color: red;
}
</style>
