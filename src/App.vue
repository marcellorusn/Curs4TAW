<script setup>
import YouDidIt from './components/YouDidIt.vue'
import BindLink from './components/BindLink.vue'
import RandomNumber from './components/RandomNumber.vue'
import Counter from './components/Counter.vue'
import BootstrapIcons from './components/BootstrapIcons.vue'
import { ref, onMounted, onUpdated } from 'vue'
const showIcons = ref(true)

onMounted(() => console.log('App mounted'))
onUpdated(() => console.log('App updated'))


const students = ref([
  { name: 'Miriam', grade: 10 },
  { name: 'Leo', grade: 9 },
  { name: 'Patrick', grade: 8 },
  { name: 'Andrei', grade: 7 }
])
</script>

<template>
  <YouDidIt />
  <BindLink />
  <RandomNumber />
  <Counter />
  <BootstrapIcons />
  <input type="checkbox" v-model="showIcons" />
  <div v-if="showIcons">
    <BootstrapIcons v-for="(icon, index) of [1, 2, 3]" :key="index" />
  </div>

  <hr>
  <h3>Test v-for</h3>
  <ul>
    <li v-for="(student, index) in students" :key="index">
      Name {{ student.name }} → Grade {{ student.grade }}
    </li>
  </ul>
</template>

<style>
@import "bootstrap-icons/font/bootstrap-icons.css";
@import "tailwindcss/tailwind.css";
</style>
