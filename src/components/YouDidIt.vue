<script setup>
import { ref } from 'vue'
const message = ref("Hello from Vue 3!")

const clickHandler = () => {
  message.value = "Button clicked!"
}
</script>

<template>
  <h1 class="text-2xl font-bold mb-4">You did it!</h1>

  <button @click="clickHandler" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600 mb-4">
    Click me
  </button>

  <p class="mb-4">{{ message }}</p>

  <input type="text" v-model="message" @change="console.log('Text changed')"
    @input="console.log('You have typed: ' + $event.target.value)" @keydown="console.log('You pressed: ' + $event.key)"
    class="border border-gray-300 rounded px-3 py-2 w-full max-w-sm" />
</template>
