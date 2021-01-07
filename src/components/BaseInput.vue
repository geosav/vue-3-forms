<template>
  <label v-if="label">{{ label }}</label>
  <input
    v-bind="$attrs"
    :value="modelValue"
    :placeholder="label"
    @input="$emit('update:modelValue', $event.target.value)"
    class="field"
  >
</template>

<script>
export default {
  props: {
    label: {
      default: '',
      type: String
    },
    modelValue: {
      type: [String, Number],
      default: ''
    }
  }
}
</script>
