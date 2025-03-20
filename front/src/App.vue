<script setup lang="ts">

import { ref } from 'vue';

const nombre = "Henry Quel";
const carnet = "202004071";
const curso = "Analisis y Diseño de Sistemas 1";
const mostrar = ref(false);
</script>

<template>
  <div style="text-align: center; margin-top: 50px;">
    <button @click="mostrar = true">Mostrar Información</button>
    <div v-if="mostrar">
      <p><strong>Nombre:</strong> {{ nombre }}</p>
      <p><strong>Carnet:</strong> {{ carnet }}</p>
      <p><strong>Curso:</strong> {{ curso }}</p>
    </div>
  </div>
</template>

<style scoped>
.button {
  background-color: #4CAF50;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
}
</style>