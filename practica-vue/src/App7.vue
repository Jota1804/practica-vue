<script setup>
// aca  importamo con lo que trabajaremos
import { ref } from "vue";

// inicializamos la variable como reactiva
let counter = ref(0);

const increment = () => {
  console.log("incrementando");
  // debemos trabajar con value, porque se vuelve un objeto
  counter.value++;
};

const decrement = () => {
  console.log("decrementando");
  // debemos trabajar con value, porque se vuelve un objeto
  counter.value--;
};

const reset = () => {
  console.log("reset");
  counter.value = 0;
};
</script>

<template>
  <h1>hello word</h1>

  <!-- aca por defecto nos muestra el value -->
  <!-- agregamos los : para que sea reactivo  -->
  <h2 :class="counter > 0 ? 'active' : 'desactive'">{{ counter }}</h2>
  <button v-on:click="increment">Incrementar</button>
  <button v-on:click="decrement">decrementando</button>
  <button v-on:click="reset">reset</button>
</template>

<style>
h1 {
  color: red;
}

.active {
  color: green;
}

.desactive {
  color: red;
}
</style>
