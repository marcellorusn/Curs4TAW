<script setup>
import { useTask } from '@/stores/task';
const taskStore = useTask();
import { ref } from 'vue';
const newTaskTitle = ref('');

const isAddingTask = ref(false);

const addNewTask = () => {
    taskStore.addTask({
        id: Math.floor(Math.random()*10000),
        title: newTaskTitle.value,
        done: false,
        favorite: false
    });
    isAddingTask.value = false;

};


</script>

<template>
    <div v-if="!isAddingTask">
        <button type="button" class="bg-yellow-300 text-black px-2 rounded ml-4" @click="isAddingTask = true">
            Add new task
        </button>
    </div>

    <div v-else>
        <input type="text" placeholder="Enter task description..."
            class="border border-gray-300 rounded px-2 py-1 ml-4" v-model="newTaskTitle">
        <button type="button" class="bg-green-500 text-white px-2 rounded ml-2" @click="addNewTask">
            Save
        </button>
        <button type="button" class="bg-red-500 text-white px-2 rounded ml-2" @click="isAddingTask = false">
            Cancel
        </button>
        </input>
    </div>
</template>