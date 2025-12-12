<script setup>
import {useTask} from '@/stores/task.js'
const taskStore = useTask();

import TaskList from '@/components/tasks/TaskList.vue'

</script>
<template>

    <TaskList />

</template>