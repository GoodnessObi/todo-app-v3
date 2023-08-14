<script setup lang="ts">
import NewTodo from '@/components/Todo/NewTodo.vue'
import TodoList from '@/components/Todo/TodoList.vue'
import type { todo } from '@/types'
import { computed } from 'vue'

const res = await fetch('https://jsonplaceholder.typicode.com/todos')
const allTodos = await res.json()

const todos = computed<todo[]>(() => {
  return allTodos.filter((todo: todo) => todo.userId === 1)
})
</script>

<template>
  <div>
    <NewTodo />
    <TodoList :todos="todos" />
  </div>
</template>
