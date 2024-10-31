<script setup>
// aca  importamo con lo que trabajaremos
import { ref, computed } from "vue";

// inicializamos la variable como reactiva
let counter = ref(0);

let arrayFavoritos = ref([]);

const increment = () => {
  // debemos trabajar con value, porque se vuelve un objeto
  counter.value++;
};

const decrement = () => {
  // debemos trabajar con value, porque se vuelve un objeto
  counter.value--;
};

const reset = () => {
  counter.value = 0;
};

const add = () => {
  arrayFavoritos.value.push(counter.value);
};

const bloquearBtn = computed(() => {
  const numSearch = arrayFavoritos.value.find((num) => num === counter.value);
  console.log(numSearch);
  if (numSearch === 0) return true;
  return numSearch ? true : false;
});

// con el computado podemos medir varias opciones, y podemos hacerlo asincrono
const classComputed = computed(() => {
  if (counter.value === 0) {
    return "zero";
  }

  if (counter.value > 0) {
    return "active";
  }

  if (counter.value < 0) {
    return "desactive";
  }
});
</script>

<template>
  <h1>hello word</h1>

  <h2 :class="classComputed">{{ counter }}</h2>
  <button v-on:click="increment">Incrementar</button>
  <button v-on:click="decrement">decrementando</button>
  <button v-on:click="reset">reset</button>
  <button v-on:click="add" :disabled="bloquearBtn">add</button>
  <br />
  <ul>
    <li v-for="(num, index) in arrayFavoritos" :key="index">
      {{ num }}
    </li>
  </ul>
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

.zero {
  color: peru;
}
</style>
