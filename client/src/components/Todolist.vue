<template>
  <div class="todolist">
    <h3>{{title}}<button>x</button></h3>
    <div>
      <input>
      <button>+</button>
    </div>
    <ul>
      <li v-for="(task) in tasks" :key="task.id">
        <input type="checkbox" :checked="task.isDone">
        <span>{{task.title}}</span>
        <button @click="removeTaskHandler(task.id)">✖️</button>
      </li>
    </ul>
    <button>All</button>
    <button>Active</button>
    <button>Completed</button>
  </div>
</template>

<script>
/* eslint-disable */

export default {
  name: "Todolist",
  props: {
    title: {
      type: String,
      required: true
    },
    tasks: {
      id: {
        type: Number,
        required: true
      },
      title: {
        type: String,
        required: true
      },
      isDone: {
        type:Boolean,
        required: true
      }
    },
  },
  methods: {
    removeTaskHandler(taskId) {
      this.$emit('removeTask', taskId)
    }
  }
}
</script>

<style>
.todolist {
  padding: 30px;
}
</style>