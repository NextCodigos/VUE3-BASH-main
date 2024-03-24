<!-- Interpolacion de texto -->

<script setup>
const name ='Vue Dinamico';
const stylecolor = "color:blue";
const arrayColores = ["blue","red","peru"]
// Sino defino me sale inactivo
const activo = true
// const activo = false

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
<!-- COn array de colores pongo el indice y cambia el color del texto -->
  <h2 :style="`color: ${arrayColores[0]}`">Soy peru</h2>
  <h2 :style="`color: ${arrayColores[1]}`">Soy peru</h2>
  <h2 :style="`color: ${arrayColores[2]}`">Soy peru</h2>

  <!-- Vemos texto de arrayColores -->
<h2>{{ arrayColores }}</h2>

<!-- TErnario -->
<h2>{{ activo ? "Estoy activo" : "Estoy inactivo" }}</h2>

<!-- Directivas  el else despues de l if-->
<!-- Cuando se hacen poco cambios -->
<h2 v-if="activo === true">
<span>iconos</span>
Estoy activo
</h2>
<h2 v-else-if="!activo === false">Estoy inactivo</h2>
<h2 v-else-if="activo === true">Estoy inactivo</h2>
<h2 v-else="activo">Estoy inactivo</h2>

<!-- v-show Para ociltar cosas mas a menudo-->
<h2 v-show="activo">Estoy activo v-show</h2>

</template>

<style>
h1{
  color: rebeccapurple;
}</style>
