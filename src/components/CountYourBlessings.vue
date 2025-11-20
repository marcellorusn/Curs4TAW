<script setup>
const props = defineProps(['startCount'])
    
import { ref } from 'vue'
const counter = ref(props.startCount || 0)

    counter.value++


</script>

<template>
    <hr class="my-4 border-gray-300">
    <h3 class="text-xl font-semibold mb-2">Counter</h3>

    <button @click="counter++" class="bg-blue-500 text-white px-4 py-2 rounded mr-2 hover:bg-blue-600">
        Increment v1
    </button>

    <button @click="incrementCounter" class="bg-green-500 text-white px-4 py-2 rounded hover:bg-green-600">
        Increment v2
    </button>

    <div class="mt-2 text-lg font-medium">Value: {{ counter }}</div>

    <hr class="my-4 border-gray-300">
    <h3 class="text-xl font-semibold mb-2">
        Bootstrap Icons <i class="bi bi-airplane-engines text-2xl"></i>
    </h3>
</template>
