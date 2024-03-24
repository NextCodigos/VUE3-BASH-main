<!-- Interpolacion de texto -->

<script setup>
const name ='Vue Dinamico';

// Crear un array de frutas
var arrayFrutas1 = ["manzana", "banana", "uva", "pera", "sandía"];

// Crear el array de frutas con objetos
var arrayFrutas = [
  {
    nombre: "Manzana",
    precio: 1.00,
    descripcion: "Una fruta deliciosa y saludable."
  },
  {
    nombre: "Banana",
    precio: 0.50,
    descripcion: "Una fruta tropical llena de energía."
  },
  {
    nombre: "Uva",
    precio: 2.50,
    descripcion: "Pequeñas y jugosas frutas en racimos."
  }
];

</script>

<template>
  
<ul>
  <!-- Asi no es dinamico -->
  <!-- <li>{{ arrayFrutas[0] }}</li>
  <li>{{ arrayFrutas[1] }}</li>
  <li>{{ arrayFrutas[2] }}</li>
  -->
<!-- Ejemplo uno de mostrar array con v-for -->
  <!-- <li v-for="(fruta,index) in arrayFrutas">
    {{ index }} - {{ fruta }}
  </li>
</ul> -->

<!-- Con key -->
  <li v-for="fruta in arrayFrutas"
  :key="fruta.nombre">
  {{ fruta.nombre }} - {{ fruta.precio }} - {{ fruta.descripcion }}  
  </li>
</ul>



</template>

<style>
h1{
  color: rebeccapurple;
}</style>
