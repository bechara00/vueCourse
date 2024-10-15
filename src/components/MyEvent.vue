<script setup>
import { ref } from 'vue'
let count = ref(0)

const incremet = () => count.value++

const decrement = () => count.value--

const reset = () => (count.value = 0)

const submithandler = e => {
  e.preventDefault()
  console.log('Valid Credentials', e.value)
}
</script>

<template>
  <h1>My Event</h1>
  <h2>Count: {{ count }}</h2>
  <button @click="incremet">increment</button>
  <button @click="decrement">decrement</button>
  <button @click="reset">Reset Count</button>
  <form @submit="submithandler">
    <input type="text" placeholder="Enter your name" />
    <input type="email" placeholder="Enter your email" />
    <button type="submit">Submit</button>
  </form>
</template>
