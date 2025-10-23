<script setup>
import { ref, onMounted, onUpdated } from 'vue'

const message = ref('Hello from Vue !')

const clickHandler = () => {
  console.log('Button clicked!')
}

const changeHandler = () => console.log('You changed me!')
const inputHandler = (e) => console.log('You typed: ' + e.target.value)
const keydownHandler = (e) => console.log('You pressed: ' + e.key)

onMounted(() => console.log('App mounted'))
onUpdated(() => console.log('App updated'))
</script>

<template>
  <h1>{{ message }}</h1>

  <button @click="clickHandler">Click me</button>
  <br />
  <p>
    <input 
      @change="changeHandler" 
      @input="inputHandler($event)" 
      @keydown="keydownHandler($event)"
      type="text" 
    />
  </p>
</template>

<style scoped>
/* #app {
  text-align: left;
  margin-top: 4rem;
  color: rgb(212, 24, 143);
} */
</style>
