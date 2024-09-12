<template>
  <p style="font-size: 30px;"> Count: {{ count }}</p>
  <button v-on:click="increment" style="background-color: cyan; font-size: 30px; margin-left: 20px">+</button>
  <button v-on:click="decrement" style="background-color: cyan; font-size: 30px;">-</button>
</template>

<script setup>
import { ref } from 'vue';
let count = ref(0);

const increment = () => count.value++;
const decrement = () => count.value--;
</script>
