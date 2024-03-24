<script setup>
import { ref } from 'vue'

const name = 'Vue Dinámico';

// Creamos variable reactiva
const counter = ref(0)

// Métodos o funciones

// const incremento = () => {
//   console.log('Aumentar contador')
//   counter.value++
//   console.log(counter.value)
// }
const incremento = () =>  counter.value++



// const decremento = () => {
//   console.log('Disminuir contador')
//   counter.value--

const decremento = () =>counter.value--


// const resetearContador = () => {
//   console.log('Restablecer contador a cero')
//   counter.value = 0
// }
const resetearContador = () => (counter.value = 0)

</script>

<template>
  <!-- Así es dinámico -->
  <div>
    <h1>Hola {{ name.toLocaleUpperCase() }}</h1>
    <h2 :class="counter > 0 ? 'positive' : 'negativo'">{{ counter }}</h2>
    <button @click="incremento">Aumentar</button>
    <button @click="decremento">Decremento</button>
    <button @click="resetearContador">Restablecer a Cero</button>
  </div>
</template>

<style>
h1 {
  color: rebeccapurple;
}
.positive{
  color:red;
}
.negativo{
  color:green;
}
.cero{
  color:aquamarine
}
</style>
