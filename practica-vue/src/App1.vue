<script setup>
const name = "Nombre variable";
const stylerColor = "color: blue";
const activo = false;
</script>

<template>
  <h1>hello word {{ name }}</h1>
  <!-- el v-bind se puede recortar solo colocando : -->
  <h2 :style="stylerColor">soy azul</h2>
  <!-- <h2 v-bind:style="stylerColor">soy azul</h2> -->
  <p v-if="activo">estoy activo</p>
  <!-- estos deben ir seguidos para poder trabajar -->
  <p v-else="!activo">estoy inactivo</p>
</template>

<!-- si algo se va a ocultar y mostrar con frecuencia, es mejor hacerlo con v-show. porque consume menos -->

<style>
h1 {
  color: red;
}
</style>
