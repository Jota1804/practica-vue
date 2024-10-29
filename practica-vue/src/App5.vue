<script setup>
const frutas = [
  {
    name: "manzana",
    price: "1$",
    description: "Una manzana",
    stock: "0",
  },
  {
    name: "pera",
    price: "1.2$",
    description: "Una pera",
    stock: "10",
  },
  {
    name: "mora",
    price: "1.5$",
    description: "Una mora",
    stock: "10",
  },
];
</script>

<template>
  <h1>hello word</h1>

  <!-- para poder correr un v-if dentro de un v-for -->
  <ul>
    <template v-for="fruta in frutas">
      <li v-if="fruta.stock > 0">{{ fruta.name }} - {{ fruta.price }}</li>
    </template>
  </ul>
</template>

<style>
h1 {
  color: red;
}
</style>
