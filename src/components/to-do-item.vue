<template>
  <li class="task">
    <div class="round">
      <input type="checkbox" class="visually-hidden" :id="todo.id">
      <label :for="todo.id">
        <span>{{todo.text}}</span>
      </label>
    </div>

  </li>
</template>

<script>


export default {
  name: "to-do-item",
  props: ['todo'],
  data() {
    return {}
  },

  computed: {}
}
</script>