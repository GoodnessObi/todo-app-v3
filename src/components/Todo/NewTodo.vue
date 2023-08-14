<script setup lang="ts">
import Button from '../UIcomponents/Button.vue'
import InputField from '../UIcomponents/InputField.vue'
</script>

<template>
  <div :class="$style.todoForm">
    <InputField type="text" id="newTodo" />
    <Button type="primary">
      <template #text>Add</template>
    </Button>
  </div>
</template>

<style module>
.todoForm {
  border-bottom: 1px solid #4c4b16;
  padding-bottom: 1rem;
}
</style>
