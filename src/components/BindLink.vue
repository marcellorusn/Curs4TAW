<script setup>
import { ref } from 'vue'
const link = ref('https://emanuel.ro/')
const target = ref('_blank')
</script>


<template>
    <br>
    <a :href="link" target="_blank">Visit Emanuel website</a>
    <br>
</template>