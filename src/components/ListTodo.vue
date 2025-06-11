<script setup>
import { ref } from 'vue'

const botonText = ref('')
const arrayText = ref([])

function addTask() {
 const texto = nuevaTarea.value.trim()
 if (texto === '') return

  tareas.value.push(texto)
  nuevaTarea.value = ''
}
</script>

<template>
  <h1 class="card">Lista To-do</h1>
   <input
      v-model="nuevaTarea"
      @keyup.enter="addTask"
      placeholder="Escribe una tarea"
    />
    <button @click="cambiarTexto">add task</button>
    <ul>
      <li v-for="(tarea, index) in tareas" :key="index">
      {{tarea}}
      </li>
    </ul>

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