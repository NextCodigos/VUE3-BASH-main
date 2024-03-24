<script setup>
import ArrayColores from './ArrayColores.vue'
import ArrayFrutas from './ArrayFrutas.vue'
import ArrayOobjetos from './Array-oobjetos.vue'
import ArrayOobjetosID from './Array-oobjetos-ID.vue'
import Computed from './Computed.vue'
import ComputedCONFuncion from './Computed-CON-FUncion.vue'
import ContadorColor from './Contador-Color.vue'
import ContadorColor2 from './Contador-Color2.vue'
import Eventos1 from './Eventos1.vue'
import Eventos2 from './Eventos2.vue'
import RecorrerObjeto from './RecorrerObjeto.vue'
import ReactividadContador from './Reactividad-Contador.vue'
import VBindVShowIfElseIf from './V-bind-V-show-If-ElseIf.vue'
import VForVIf from './V-For-V-If.vue'
import VForFrutas from './V-for-Frutas.vue'
import VBind from './Vbind.vue'
import { ref } from 'vue'

const name = 'Vue Dinámico';

// Creamos variable reactiva
const counter = ref(0)

// Métodos o funciones

const incremento = () => counter.value++

const decremento = () => counter.value--

const resetearContador = () => (counter.value = 0)

const getClassCounter = () => {
  if (counter.value === 0) {
    return 'cero'
  } else if (counter.value > 0) {
    return 'positive'
  } else {
    return 'negativo'
  }
}
</script>

<template>
  <!-- Así es dinámico -->
  <div>
    <h1>Hola {{ name.toLocaleUpperCase() }}</h1>

    <h2 :class="getClassCounter()">{{ counter }}</h2>
    <button @click="incremento">Aumentar</button>
    <button @click="decremento">Decremento</button>
    <button @click="resetearContador">Restablecer a Cero</button>
  </div>
  <ArrayColores />
  <ArrayFrutas />
  <ArrayOobjetos />
  <ArrayOobjetosID />
  <Computed />
  <ComputedCONFuncion />
  <ContadorColor />
  <ContadorColor2 />
  <Eventos1 />
  <Eventos2 />
  <RecorrerObjeto />
  <ReactividadContador />
  <VBindVShowIfElseIf />
  <VForVIf />
  <VForFrutas />
  <VBind />
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
  color: blue;
}
</style>
