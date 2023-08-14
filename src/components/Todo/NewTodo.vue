<script setup>
import Button from '../UIcomponents/Button.vue'
</script>

<template>
  <div>
    <input type="text" />
    <Button>
      <template #text>Add</template>
    </Button>
  </div>
</template>
