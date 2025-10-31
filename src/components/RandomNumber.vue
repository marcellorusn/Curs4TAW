<script setup>
import { ref } from 'vue'

const randomNumber = ref(null)
const updateRandomNumber = () => {
    randomNumber.value = Math.random()
}
</script>

<template>
    <hr class="my-4 border-gray-300">

    <h3 class="text-xl font-semibold mb-3">Display a random number</h3>

    <button @click="updateRandomNumber" class="bg-purple-500 text-white px-4 py-2 rounded hover:bg-purple-600 mb-3">
        Get a random number: {{ randomNumber }}
    </button>

    <div v-if="randomNumber" class="mb-2">
        <div v-if="randomNumber > 0.5" class="text-green-600 font-medium">
            Number is bigger or equal to 0.5
        </div>
        <div v-else class="text-red-600 font-medium">
            Number is lower or equal to 0.5
        </div>
    </div>

    <div v-if="randomNumber && randomNumber >= 0.5" class="text-green-700 mt-2">
        Number is bigger or equal to 0.5
    </div>
    <div v-else-if="randomNumber" class="text-red-700 mt-2">
        Number is lower or equal to 0.5
    </div>

    <br>
</template>
