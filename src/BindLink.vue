<script setup>
import { ref } from 'vue'
const message = ref('Hello from Vue !')
const link = ref('https://emanuel.ro')
</script>
<template>
    <h3 class="inline-block bg-purple-300 rounded-2xl outline-1 mb-4">
        Bind link example
    </h3>

    <p>
        <a :href="link" target="_blank">{{ message }}</a>
    </p>
</template>