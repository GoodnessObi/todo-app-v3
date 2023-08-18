<script>
import CustomBtn from '../UIcomponents/CustomBtn.vue'
import InputField from '../UIcomponents/InputField.vue'

export default {
  components: {
    CustomBtn,
    InputField
  }
}
</script>

<template>
  <div :class="$style.todoForm">
    <InputField type="text" id="newTodo" />
    <CustomBtn type="primary">
      <template #text>Add</template>
    </CustomBtn>
  </div>
</template>

<style module>
.todoForm {
  border-bottom: 1px solid #4c4b16;
  padding-bottom: 1rem;
}
</style>
