<script setup>
import { useTask } from '@/stores/task.js'
const taskStore = useTask();

defineProps({
    taskId: {
        type: Number,
        required: false
    },
    isFavorite: {
        type: Boolean,
        required: false
    }
});
</script>

<template>
    <div>
        <button class="cursor-pointer mr-2" @click="taskStore.toggleFavorite(taskId)">
            <i class="bi" :class="isFavorite ? 'bi-star-fill text-yellow-500' : 'bi-star'"></i>
        </button>
        <button class="cursor-pointer" @click=" taskStore.removeTask(taskId)">
            <i class="bi bi-trash"></i>
        </button>
    </div>
</template>