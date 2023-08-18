<script>
export default {
  props: {
    type: String,
    id: String
  }
}
</script>

<template>
  <input :class="$style.input" type="{{ type }}" id="{{ id }}" name="{{ id }}" />
</template>

<style module>
.input {
  border: 1px solid #b3c890;
  padding: 0.5rem 1rem;
  font-size: 1.25rem;
  width: 100%;
  border-radius: 4px;
  margin-bottom: 0.5rem;
}

.input:focus-visible {
  outline: #73a9ad;
}
</style>
