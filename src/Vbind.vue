<!-- Interpolacion de texto -->

<script setup>
const name ='Vue Dinamico';
const stylecolor = "color:blue";

</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <!-- Asi va bien -->
  <!-- <h2 style="color:blue">Soy azul</h2> -->

  <!-- Asi no va bien -->
  <!-- <h2 style="{{ stylecolor }}">Soy azul</h2> -->

  <!-- ASi podemos poner la variable del color -->
  <h2 v-bind:style="stylecolor">Soy azul</h2>
  <!-- Atajo de arriba de v-bind -->
  <h2 :style="stylecolor">Soy azul</h2>



</template>

<style>
h1{
  color: rebeccapurple;
}</style>
