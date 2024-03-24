<script setup>
import { ref } from 'vue'

const name = 'Vue Dinámico';

// Creamos variable reactiva
const counter = ref(0)

// Métodos o funciones

const incremento = () => {
  console.log('Aumentar contador')
  counter.value++
  console.log(counter.value)
}

const decremento = () => {
  console.log('Disminuir contador')
  counter.value--
}

const resetearContador = () => {
  console.log('Restablecer contador a cero')
  counter.value = 0
}
</script>

<template>
  <!-- Así es dinámico -->
  <div>
    <h1>Hola {{ name.toLocaleUpperCase() }}</h1>
    <h2>{{ counter }}</h2>
    <button @click="incremento">Aumentar</button>
    <button @click="decremento">Decremento</button>
    <button @click="resetearContador">Restablecer a Cero</button>
  </div>
</template>

<style>
h1 {
  color: rebeccapurple;
}
</style>
