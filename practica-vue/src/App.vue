<script setup>
const handleClick = (message) => {
  // console.log("diste click");
  console.log(message);
};
</script>

<template>
  <h1>hello word</h1>
  <!-- para trabajar con eventos
  <button v-on:click="handleClick">Click me</button> -->
  <!-- se puede abrebiar con el @ -->
  <!-- <button @:click="handleClick('message 1')">Click me</button> -->

  <!-- existen modificadores -->
  <!-- existe el prevent default tambien -->
  <button v-on:click.left.prevent="handleClick('message izquierdo')">
    Click izquierdooo
  </button>
  <button @click.middle="handleClick('message medio')">Click medio</button>
  <button @click.right="handleClick('message derecho')">Click derecho</button>
</template>

<style>
h1 {
  color: red;
}
</style>
