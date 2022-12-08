<template>
  <div class="app">
    <Todolist
        title="What to learn"
        :tasks="tasks"
        @removeTask=removeTask
    />
  </div>
</template>

<script>

import Todolist from "@/components/Todolist";
export default {
  name: 'App',
  components: {Todolist},
  data(){
    return {
      tasks: [
        {id: 1, title: 'HTML&CSS', isDone: true},
        {id: 2, title: 'VUE', isDone: false},
        {id: 3, title: 'NODE', isDone: false},
        {id: 4, title: 'MongoDB', isDone: false},
      ],
    }
  },
  methods: {
    removeTask(taskId){
      this.tasks = this.tasks.filter( el => el.id !== taskId )
    },
  }
}
</script>

<style>
.app {
  padding: 30px;
  display: flex;
}
</style>
