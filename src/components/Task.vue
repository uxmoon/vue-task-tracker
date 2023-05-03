<template>
  <div :class="[task.reminder ?'reminder':'', 'task']">
    <h3>
      {{ task.text }}
      <i @click="onDelete(task.id)" class="fa-solid fa-xmark"></i>
    </h3>
    <p>{{ task.day }}</p>
  </div>
</template>

<script>
export default {
  name: 'Task',
  props: {
    task: Object
  },
  methods: {
    onDelete(id) {
      this.$emit('delete-task', id)
    }
  }
}
</script>

<style scope>
.fa-solid {
  color: darkred;
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