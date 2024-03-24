<script setup>
const name = 'Vue Dinámico';

// Métodos
const handleClick = () => {
  console.log("Me diste click");
}
const handleClick2 = (message) => {
  console.log(message);
}
</script>

<template>
  <!-- ASi no es dinamico -->
  <div>
    <h1>Hola {{ name.toLocaleUpperCase() }}</h1>
    <button v-on:click="handleClick()">Actívame 1</button>
    <button @click="handleClick()">Actívame 2</button>
  </div>
  
  <!-- ASi es dinamico -->
  <div>
    <h1>Hola {{ name.toLocaleUpperCase() }}</h1>
    <button v-on:click="handleClick2('Texto 1')">Actívame 1</button>
    <button @click="handleClick2('Texto 2')">Actívame 2</button>
  </div>
</template>

<style>
h1 {
  color: rebeccapurple;
}
</style>
