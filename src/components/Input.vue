<template>
  <br />
  <input
    type="text"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
  />
  <p>Input</p>
</template>

<script>
export default {
  name: 'App-Input',
  props: {
    modelValue: String, // modelValue 為系統名稱，不能自由命名
  },
};
</script>
