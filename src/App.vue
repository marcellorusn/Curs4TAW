<script setup>
import { ref, onMounted, onUpdated } from 'vue'

const message = ref('Hello from Vue !')

const clickHandler = () => {
  console.log('Button clicked!')
}

const changeHandler = () => console.log('You changed me!')
const inputHandler = (e) => console.log('You typed: ' + e.target.value)
const keydownHandler = (e) => console.log('You pressed: ' + e.key)
const link = ref('https://emanuel.ro')
const randomNumber = ref(null)
const counter = ref(0)
const incrementCounter = () => {
  counter.value++
}

const updateRandomNumber = () => {
  randomNumber.value = Math.random()
}

onMounted(() => console.log('App mounted'))
onUpdated(() => console.log('App updated'))
</script>

<template>
  <i class="bi bi-brightness-high"></i>
  <h1>{{ message }}</h1>

  <button @click="clickHandler">Click me</button>

  <p>{{ message }}</p>

  <br />

  <input type="text" v-model="message" @change="changeHandler" @input="inputHandler($event)"
    @keydown="keydownHandler($event)" />

  <br /><br />

  <a :href="link" target="_blank">Visit Emanuel</a>

  <hr />

  <h3>Display a random number</h3>
  <button @click="updateRandomNumber">Get a random number{{randomNumber}}</button>

  <div v-if="randomNumber">
    <div v-if="randomNumber >= 0.5">
      The random number is greater than 0.5
    </div>
    <div v-else>
      The random number is less than  0.5
    </div>
  </div>
  <br>
   <div v-if="randomNumber && randomNumber >= 0.5">
      The random number is greater than 0.5
    </div>
    <div v-else-if="randomNumber">
      The random number is less than  0.5
    </div>

    <br>
    <hr>
    <h3> Counter </h3>
    <button @click="counter++">Increment</button>
    <div>{{counter}}</div>
</template>


<style>

@import "tailwindcss";
@import "bootstrap-icons";
</style>
/* #app {
  text-align: left;
  margin-top: 4rem;
  color: rgb(212, 24, 143);
} */

