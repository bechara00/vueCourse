<script setup>
console.log('Hola mundo')
import AnotherComponent from './AnotherComponent.vue'
</script>

<template>
  <h1>This is a parent component</h1>
  <AnotherComponent />
</template>

<style scoped>
h1 {
  color: red;
}
</style>
