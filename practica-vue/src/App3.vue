<script setup>
const frutas = [
  {
    name: "manzana",
    price: "1$",
    description: "Una manzana",
  },
  {
    name: "pera",
    price: "1.2$",
    description: "Una pera",
  },
  {
    name: "mora",
    price: "1.5$",
    description: "Una mora",
  },
];
</script>

<template>
  <h1>hello word {{ name }}</h1>
  <!-- {{ frutas }} -->
  <ul>
    <!-- <li v-for="(fruta, index) in frutas">{{ fruta }}</li> -->
    <!-- podemos usar el indice, agregandolo -->
    <!-- la key debemos agregarlo, debe ser unico. como un id -->
    <li v-for="fruta in frutas" :key="fruta.name">
      {{ fruta.name }} - {{ fruta.price }} - {{ fruta.description }}
    </li>
  </ul>
</template>

<style>
h1 {
  color: red;
}
</style>
