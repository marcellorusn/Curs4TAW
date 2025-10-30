<script setup>
import { ref } from 'vue'

const message = ref('You did it !')
</script>



<template>
  <h1 class="text-3xl font-bold text-blue-600">{{ message }}</h1>
    <button @click="console.log('You did it!')">Click me</button>
    <br />
    <input @change="console.log('You changed me!')" @input="console.log('You typed: ' + $event.target.value)"
      @keydown="console.log('You pressed: ' + $event.key)" type="text" />
</template>
