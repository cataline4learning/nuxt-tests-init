<template>
  <button class="button" :type="type" @click="$emit('click')">
    {{ text }}
  </button>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    text: {
      type: String,
      required: true
    },
    type: {
      type: String,
      default: 'button',
      validator: (value) => {
        return ['button', 'submit'].includes(value)
      },
    },
  },
})
</script>

<style lang="scss" scoped>
.button {
  background-color: #2d6cea;
  color: #fff;
  padding: 0.5rem;
  border-radius: 0.5rem;
  width: max-content;
  cursor: pointer;
}
</style>
