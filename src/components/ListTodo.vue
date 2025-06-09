<script setup>
import { ref } from 'vue'

const botonText = ref('dar click')

function cambiarTexto() {
  botonText.value = 'gracias por dar click'
}
</script>

<template>
  <h1 class="card">Lista To-do</h1>
  <button @click="cambiarTexto">{{ botonText }}</button>
</template>

<style scoped>
.card {
  padding: 1rem;
  border-radius: 8px;
  text-align: center;
}
button {
  padding: 0.5rem 1rem;
  background-color: #42b883;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
</style>