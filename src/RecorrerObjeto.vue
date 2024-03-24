<!-- Interpolacion de texto -->

<script setup>
const name = 'Vue Dinamico';

// Crear un array de frutas
var arrayFrutas1 = ["manzana", "banana", "uva", "pera", "sandía"];

// Crear Objeto de  una fruta
var objetoFrutas =
{
  nombre: "Manzana",
  precio: 1.00,
  descripcion: "Una fruta deliciosa y saludable.",
  id: 1
}


</script>

<template>
  <h1>Hola {{ name.toLocaleUpperCase() }}</h1>
  {{ objetoFrutas }}
  <ul>

    <!-- Con key -->
    <li v-for="(value, propiedad, index) in objetoFrutas" :key="value">
      {{ index }} - {{ propiedad }}: {{ value }}
    </li>

  </ul>
</template>

<style>
h1 {
  color: rebeccapurple;
}
</style>
