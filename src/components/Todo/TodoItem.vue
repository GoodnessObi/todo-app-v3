<script setup lang="ts">
import type { todo as todoItem } from '@/types'
import Button from '../UIcomponents/Button.vue'

defineProps<{ todo: todoItem }>()
</script>

<template>
  <div>
    <input type="checkbox" name="" id="" />
    {{ todo.title }}
    <Button>
      <template #text>Delete</template>
    </Button>
  </div>
</template>
