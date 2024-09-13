<template>
  <p>Count: {{ count }}</p>
  <button v-on:click="increment">+</button>
  <button v-on:click="addTen">+10</button>
  <button v-on:click="decrement" style="background-color: gray">-</button>
  <button v-on:click="subtractTen" style="background-color: gray">-10</button>
  <br />
  <br />
  <br />
  <button v-on:click="reset">Reset</button>
</template>

<script setup>
import { ref } from 'vue'

let count = ref(0)

const increment = () => count.value++
const addTen = () => (count.value += 10)
const decrement = () => count.value--
const subtractTen = () => (count.value -= 10)
const reset = () => (count.value = 0)
</script>

<style>
p {
  font-size: 30px;
}

button {
  background-color: cyan;
  font-size: 30px;
  margin-left: 20px;
}
</style>
