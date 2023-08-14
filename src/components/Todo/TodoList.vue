<script setup lang="ts">
import type { todo } from '@/types'
import TodoItem from './TodoItem.vue'

defineProps<{
  todos: todo[]
}>()
</script>

<template>
  <div v-for="todo in todos" :key="todo.id">
    <TodoItem :todo="todo" />
  </div>
</template>
