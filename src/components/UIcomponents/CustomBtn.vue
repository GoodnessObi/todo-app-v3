<script>
export default {
  props: {
    type: String
  }
}
</script>

<template>
  <button :class="`btn btn-${type}`">
    <slot name="text"></slot>
  </button>
</template>

<style scoped>
.btn {
  display: flex;
  justify-content: center;

  cursor: pointer;
}

.btn-primary {
  background-color: #1c6758;
  color: #fff;
  padding: 0.5rem 0;
  width: 100%;
  border-radius: 4px;
  font-size: 1.25rem;
}

.btn-small {
  background-color: transparent;
  border: 0;
}
</style>
