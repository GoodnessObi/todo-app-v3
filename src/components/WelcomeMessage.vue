<script>
export default {
  props: {
    msg: String
  }
}
</script>

<template>
  <div class="greetings">
    <p>"{{ msg }}"</p>
  </div>
</template>

<style scoped>
.greetings {
  text-align: center;
}

.greetings p {
  color: #21bf73;
}

@media (min-width: 1024px) {
}
</style>
