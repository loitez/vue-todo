<template>
  <div class="add-task">
    <input v-model="task" v-on:keyup.enter="$emit('addTodo', task)" ref="taskInput" type="text" placeholder="Название задачи">
    <add-button @addTask="$emit('addTodo', task)"></add-button>
  </div>
</template>

<script>
import addButton from './add-button.vue'

export default {
  name: "new-task",
  components: {
    addButton
  },
    methods: {
    },
  data() {
    return {}
  },
  props: ['todos'],
}
</script>

<style scoped>

</style>