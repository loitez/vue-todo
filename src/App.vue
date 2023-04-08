

<template>
  <div class="container">
    <h4>Today's tasks</h4>
    <ul class="tasks">
      <to-do-item
          v-for="text in todos"
          :todo="text"
          :key="text.id"
      ></to-do-item>
      <new-task @addTodo="addNewItem" :todos="todos"></new-task>


    </ul>
  </div>

</template>


<script>
import toDoItem from './components/to-do-item.vue'
import newTask from './components/new-task.vue'

export default {
  name: 'App',
  data() {
    return {
      todos: [
        { id: 0, text: 'Create To-Do-App in Vue.js', number: "0" },
        { id: 1, text: 'Send it to Vladik', number: "1"}
      ],
    }
  },
  components: {
    toDoItem,
    newTask
  },
  methods: {
    addNewItem(task) {
      this.todos.push({
        id: this.todos.at(-1).id++,
        text: task
      })
      console.log('parent - ', task)
      console.log('parent - ', this.todos)
      task = ''
    }
    /*addNewTodo() {
      console.log('working')
      const input = document.querySelector('input')
      this.todos.push({
        id: 2,
        text: input.value
      })
      input.value = ''
    }*/
  },
}
</script>


