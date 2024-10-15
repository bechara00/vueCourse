<script setup>
import { reactive } from 'vue'
let initialState = reactive({ count: 0 }) // se hace objeto porque reactive no almacena promitivos como numeros o booleanos
</script>

<template>
  <h1>Reactive Component</h1>
  <p>Con reactive no se pueden almacenar primitivos</p>
  <p>Count: {{ initialState.count }}</p>
  <button @click="initialState.count++">+</button>
  <button @click="initialState.count--">-</button>
  <button @click="initialState.count = 0">0</button>
</template>
