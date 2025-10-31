<script setup>
import { ref } from 'vue'
const link = ref('https://emanuel.ro/')
const target = ref('_blank')
</script>


<template>
    <br>
    <a :href="link" target="_blank" class="bg-red-200 text-white py-1 rounded ">Visit Emanuel website</a>
    <br>
</template>