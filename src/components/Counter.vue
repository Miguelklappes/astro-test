<template>
  <div class="counter">
    <button @click="subtract()">-</button>
    <pre>{{ count }}</pre>
    <button @click="add()">+</button>
  </div>
  <div class="children">
    <slot />
  </div>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(10);
const add = () => (count.value = count.value + 1);
const subtract = () => (count.value = count.value - 1);
</script>