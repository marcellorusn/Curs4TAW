<script setup>
const incrementCounter = () => {
    counter.value++
}
const counter = ref(0)
</script>

<template>
    <h3>
        Counter


        <button @click="incrementCounter" class="bg-yellow-200 rounded-sm">
            Increment
        </button>

        <div>{{ counter }}</div>
    </h3>
</template>