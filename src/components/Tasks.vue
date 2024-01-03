<template>
    <div :key="t.id"  v-for= "t in tasks" >
        <Task @toggle-reminder ="$emit('toggle-reminder' , t.id)" @delete-task ="$emit('delete-task',t.id)" :task=t />
    </div>

</template>

<script>
    import Task from './Task.vue';
    export default {
        name: 'Tasks',
        components: {
            Task,
        },
        props: {
            tasks: Array
        },
        emits: ['delete-task','toggle-reminder']
    }
</script>