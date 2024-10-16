<script setup>
import { reactive } from 'vue'
let initialState = reactive({ count: 0 }) // se hace objeto porque reactive no almacena promitivos como numeros o booleanos
let initialState2 = reactive({ val: { counts: 0 }, user: ['Juan', 'Bechara'] })

const changeUser = () => {
  initialState2.user[0] = 'Eliana'
  initialState2.user[1] = 'Cara'
}
</script>

<template>
  <h1>Reactive Component</h1>
  <p>Con reactive no se pueden almacenar primitivos</p>
  <p>Count: {{ initialState.count }}</p>
  <button @click="initialState.count++">+</button>
  <button @click="initialState.count--">-</button>
  <button @click="initialState.count = 0">0</button>
  <h1>Other example of ractive</h1>
  <h2>Current Count: {{ initialState2.val.counts }}</h2>
  <h2>Users: {{ initialState2.user }}</h2>
  <button @click="initialState2.val.counts += 10">Add 10</button>
  <button @click="changeUser">Change User</button>
  <button @click="initialState2.user.push('Ivan, Mathiesen')">
    Add one more
  </button>
</template>
