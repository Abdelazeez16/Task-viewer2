<template>
    <button @click="$emit('toggle-add-task')" :style="{background:color}" class="btn">{{title}}</button>
</template>

<script>
export default {
    name:'MButton',
    props: {
        title:String,
        color:String,
    },
}
</script>