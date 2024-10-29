<script setup>
const frutas = ["🥭", "🍏", "🍉", "🍌", "🍊", "🍈"];
</script>

<template>
  <h1>hello word {{ name }}</h1>
  <!-- {{ frutas }} -->
  <ul>
    <!-- <li v-for="(fruta, index) in frutas">{{ fruta }}</li> -->
    <!-- podemos usar el indice, agregandolo -->
    <li v-for="(fruta, index) in frutas">{{ index }} - {{ fruta }}</li>
  </ul>
</template>

<style>
h1 {
  color: red;
}
</style>
