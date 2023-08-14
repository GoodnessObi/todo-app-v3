<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="greetings">
    <quote>"{{ msg }}"</quote>
  </div>
</template>

<style scoped>
.greetings {
  text-align: center;
}

.greetings quote {
  color: #21bf73;
}

@media (min-width: 1024px) {
}
</style>
