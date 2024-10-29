<script setup>
const objetoFrutas = {
  name: "manzana",
  price: "1$",
  description: "Una manzana",
};
</script>

<template>
  <h1>hello word {{ name }}</h1>
  <!-- {{ frutas }} -->
  <ul>
    <!-- <li v-for="(fruta, index) in frutas">{{ fruta }}</li> -->
    <!-- podemos usar el indice, agregandolo -->
    <!-- la key debemos agregarlo, debe ser unico. como un id -->
    <!-- en la key, podemos utilizar solo fruta, dado que cada objeo aca es unico -->
    <!-- el v-if tiene mas peso que el v-for. osea, tiene mas gerarquia -->
    <li v-for="(fruta, propiedad, index) in objetoFrutas" :key="fruta">
      {{ index }} - {{ propiedad }} : {{ fruta }}
    </li>
  </ul>
</template>

<style>
h1 {
  color: red;
}
</style>
