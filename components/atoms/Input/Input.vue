<template>
  <input
    :value="value"
    :placeholder="placeholder"
    type="text"
    class="input"
    @input="$emit('input', $event.target.value)"
  />
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    value: {
      type: [String, Number],
      default: null
    },
    placeholder: {
      type: String,
      default: null
    }
  }
})
</script>

<style lang="scss" scoped>
input {
  outline: none;
  background: #fff;
  border-radius: 0.5rem;
  min-height: 36px;
  padding: 0.5rem;
  width: max-content;
  color: #000;
}
</style>
