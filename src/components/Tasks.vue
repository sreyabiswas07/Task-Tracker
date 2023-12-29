<template>
    <div :key="t.id"  v-for= "t in tasks" >
        <Task :task=t />
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
        }
    }
</script>