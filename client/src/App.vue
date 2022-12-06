<template>
  <div class="app">
    <Todolist title="What to learn" v-bind:tasks="tasks1"/>
    <Todolist title="What to buy" v-bind:tasks="tasks2"/>
  </div>
</template>

<script>

import Todolist from "@/components/Todolist";
export default {
  name: 'App',
  components: {Todolist},
  data(){
    return {
      tasks1: [
        {id: 1, title: 'HTML&CSS', isDone: true},
        {id: 2, title: 'VUE', isDone: false},
        {id: 3, title: 'NODE', isDone: false},
      ],
      tasks2: [
        {id: 1, title: 'HELLO', isDone: true},
        {id: 1, title: 'WORLD', isDone: false},
        {id: 1, title: 'YO', isDone: true},
      ],
    }
  }
}
</script>

<style>
.app {
  padding: 30px;
  display: flex;
}
</style>
