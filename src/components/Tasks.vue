<template>
    <div>
        <Task :key="task.id" v-for="task in tasks" @delete-task="$emit('delete-task',task.id)" @toggle-reminder="$emit('toggle-reminder',task.id)" :task="task"/>
    </div>
</template>

<script>
import Task from './Task.vue'

export default {
    name: 'TASKS',
    props: {
        tasks: Array
    },
    components:{
        Task
    },
    emits:['delete-task','toggle-reminder']
}
</script>