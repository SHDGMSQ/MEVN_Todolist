<template>
  <div class="todolist">
    <h3>{{title}}<button>x</button></h3>
    <div>
      <input>
      <button>+</button>
    </div>
    <ul>
      <li><input type="checkbox" :checked="tasks[0].isDone"><span>{{tasks[0].title}}</span><button>x</button></li>
      <li><input type="checkbox" :checked="tasks[1].isDone"><span>{{tasks[1].title}}</span><button>x</button></li>
      <li><input type="checkbox" :checked="tasks[2].isDone"><span>{{tasks[2].title}}</span><button>x</button></li>
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
    title: String,
    tasks: {
      id: Number,
      title: String,
      isDone: Boolean
    },
  }
}
</script>

<style>
.todolist {
  padding: 30px;
}
</style>