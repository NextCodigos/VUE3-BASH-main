<script setup>
const name = 'Vue Dinámico';

// Métodos o funciones

const handleClick2 = (message) => {
  console.log(message);
}
</script>

<template>

  <!-- ASi es dinamico -->
  <div>
    <h1>Hola {{ name.toLocaleUpperCase() }}</h1>
    <button v-on:click.right="handleClick2('Texto Right')">Actívame right</button>
    <button @click="handleClick2('Texto Left')">Actívame left</button>
    <button @click.middle="handleClick2('Texto Enmedio')">Actívame enmedio</button>
  </div>
</template>

<style>
h1 {
  color: rebeccapurple;
}
</style>
