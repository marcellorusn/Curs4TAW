<script setup>
import { useTask } from '@/stores/task';
const taskStore = useTask();

import TaskHeader from '@/components/tasks/TaskHeader.vue'
import TaskBody from '@/components/tasks/TaskBody.vue'
import TaskFooter from '@/components/tasks/TaskFooter.vue'  
</script>
<template>
  <TasksHeader />
  <TaskBody v-for="(task, index) in taskStore.tasks" :task="task" :key="index"/>
  <TaskFooter />
</template>