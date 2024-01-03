<template>
    <div :class = "[task.reminder ? 'reminder' : '', 'task']" @dblclick="$emit('toggle-reminder' , id)">
        <h3>{{ task.text }} {{ task.id }}
          <i class="fas fa-times" @click="$emit('delete-task' , id)"></i>
        </h3>
        <p>{{ task.day }} </p>
    </div>
</template>

<script>
    export default {
        name: "Task",
        props: {
            task: Object,
        },
    }
</script>

task.reminder ? 'reminder' : ''
[task.reminder ? 'reminder' : '', 'task']

<style scope>
.fas {
  color: red;
}

.task {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
}

.task.reminder {
  border-left: 5px solid green;
}

.task h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>