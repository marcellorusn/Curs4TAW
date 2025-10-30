<script setup>
import { ref } from 'vue'


const randomNumber = ref(null)


const updateRandomNumber = () => {
    randomNumber.value = Math.random()
}
</script>

<template>
    <h3 class="inline-block bg-orange-300 rounded-2xl outline-1 mb-4">
        Display a random number
    </h3>

    <p>
        <button @click="updateRandomNumber" class="bg-rose-300 rounded-sm">
            Get a random number {{ randomNumber }}
        </button>
    </p>

    <div v-if="randomNumber">
        <div v-if="randomNumber >= 0.5" class="inline-block bg-green-100">
            The random number is greater than or equal to 0.5
        </div>
        <div v-else>
            The random number is less than 0.5
        </div>
    </div>
</template>
