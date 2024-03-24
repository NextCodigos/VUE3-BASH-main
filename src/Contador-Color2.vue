<script setup>
import { ref } from 'vue'

const name = 'Vue Dinámico';

// Creamos variable reactiva
const counter = ref(0)

// Métodos o funciones

const incremento = () => counter.value++

const decremento = () => counter.value--

const resetearContador = () => (counter.value = 0)
</script>

<template>
  <!-- Así es dinámico -->
  <div>
    <h1>Hola {{ name.toLocaleUpperCase() }}</h1>
    
    <h2 :class="counter > 0 ? 'positive' : (counter < 0 ? 'negativo' : 'cero')">{{ counter }}</h2>
    <button @click="incremento">Aumentar</button>
    <button @click="decremento">Decremento</button>
    <button @click="resetearContador">Restablecer a Cero</button>
  </div>
</template>

<style>
h1 {
  color: rebeccapurple;
}

.positive {
  color: red;
}

.negativo {
  color: green;
}

.cero {
  color: aquamarine;
}</style>
