<script setup>
const handleClick = () => {
  console.log("diste click");
};
</script>

<template>
  <h1>hello word</h1>
  <!-- para trabajar con eventos -->
  <button v-on:click="handleClick">Click me</button>
</template>

<style>
h1 {
  color: red;
}
</style>
