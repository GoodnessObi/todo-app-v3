<script setup lang="ts">
import type { todo } from '@/types'
import TodoItem from './TodoItem.vue'

defineProps<{
  todos: todo[]
}>()
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
