<script setup>
import { ref, onMounted, onUpdated } from 'vue'
import YouDidIt from './YouDidIt.vue'
import BindLink from './BindLink.vue'
import RandomNumber from './RandomNumber.vue'
import Counter from './Counter.vue'

const counter = ref(0)

const students = ref([
  { name: 'Miriam', grade: 10 },
  { name: 'Marius', grade: 9 },
  { name: 'Luca', grade: 6 },
  { name: 'Ion', grade: 8 }
])





onMounted(() => console.log('App mounted'))
onUpdated(() => console.log('App updated'))
</script>

<template>

  <YouDidIt />
  <hr />
  <BindLink />
  <hr />
  <RandomNumber />
  <hr />
  <Counter />

  <i class="bi bi-brightness-high"></i>

  <hr />

  <h3>Test v-for</h3>

  <ul>
    <li v-for="(student, index) of students" :key="index" class="inline-block bg-blue-200 mb-4 mr-2 p-2 rounded-lg">
      Name {{ student.name }}, Grade {{ student.grade }}
    </li>
  </ul>
</template>

<style>
@import "tailwindcss";
@import "bootstrap-icons";
</style>
