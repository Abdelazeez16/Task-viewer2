<template>
    <header>
        <h1>{{title}}</h1>
        <Button @toggle-add-task="$emit('toggle-add-task')" :title="showAddTask ? 'close' : 'Add Task'" :color="showAddTask ? 'red' : 'green' " />
    </header>
</template>

<script>
import Button from './Button.vue'
export default {
    name:'HEADER',
    props: {
        title: String,
        showAddTask : Boolean,
    },
    components:{
        Button
    },
    emits:['toggle-add-task']
}
</script>

<style scoped>
    header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>