<script setup>
defineProps({

    task: {
        type: Object,
        required: true

    }

});

import TaskActions from './TaskActions.vue';
import TaskCheckbox from './TaskCheckbox.vue';

</script>
<template>
  <div class="grid grid-cols-8 gap-2">
    <TaskCheckbox />
    <div class="col-span-6">{{ task.title }}</div>
    <TaskActions :taskId="task.id" :isFavorite="task.favorite" />
  </div>
</template>