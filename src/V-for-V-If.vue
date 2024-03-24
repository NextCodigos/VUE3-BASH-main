<!-- Interpolacion de texto -->

<script setup>
const name = 'Vue Dinamico';
const activo=true;

// Crear un array de frutas
var arrayFrutas1 = ["manzana", "banana", "uva", "pera", "sandía"];

// Crear el array de frutas con objetos
var arrayFrutas = [
  {
    nombre: "Manzana",
    precio: 1.00,
    descripcion: "Una fruta deliciosa y saludable.",
    stock:20
  },
  {
    nombre: "Banana",
    precio: 0.50,
    descripcion: "Una fruta tropical llena de energía.",
    stock:50
  },
  {
    nombre: "Uva",
    precio: 2.50,
    descripcion: "Pequeñas y jugosas frutas en racimos.",
    stock:10
  }
];


</script>

<template>
  <h1>Hola {{ name.toLocaleUpperCase() }}</h1>
  <!-- {{ objetoFrutas }} -->
  <ul>

    <!-- Con key -->
    <!-- El v-for para recorrer array y objetos -->
    <!-- Asi meda fallo no bien ni alante ni atras -->
    <li v-if="activo" v-for="item in arrayFrutas" :key="item.nombre" >
      {{ item.nombre }} - {{ item.precio }}:
    </li>

  </ul>

  <ul>
    <li v-for="item in arrayFrutas" :key="item.name">
    <span v-if="item.stock > 0">
      {{ item.nombre }} - {{ item.precio }}
    </span>
    </li>
    </ul>

    <!-- BUENA MANERA -->
    <ul>
      <template v-for="item in arrayFrutas" :key="item.npmbre">
        <li v-if="item.stock > 0">{{ item.nombre }} - {{ item.precio }}</li>
      </template>
    </ul>
</template>

<style>
h1 {
  color: rebeccapurple;
}
</style>
