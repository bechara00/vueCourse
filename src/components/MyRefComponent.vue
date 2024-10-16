<script setup>
import { ref } from 'vue'

let count = ref(0)
</script>

<template>
  <h1>My ref component template</h1>
  <h2>Count: {{ count }}</h2>
  <button @click="count += 3">+3</button>
  <button @click="count *= 4">*4</button>
  <button @click="count = 0">reset</button>
</template>
