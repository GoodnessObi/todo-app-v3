<script>
import TodoItem from './TodoItem.vue'

export default {
  components: {
    TodoItem
  },
  props: {
    todos: Array
  }
}
</script>

<template>
  <div class="todoList">
    <TodoItem v-for="todo in todos" :key="todo.id" :todo="todo" />
  </div>
</template>

<style scoped>
.todoList {
  padding: 1rem 0;
}
</style>
