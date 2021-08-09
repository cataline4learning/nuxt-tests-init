<template>
  <ul class="list">
    <li v-for="(item, index) in items" :key="index">
      {{ item }}
    </li>
  </ul>
</template>

<script lang="ts">
import Vue, { PropType } from 'vue'

export default Vue.extend({
  props: {
    items: {
      type: Array as PropType<string[]>,
      required: true
    }
  }
})
</script>

<style lang="scss" scoped>
.list {
  margin: 0;
  li {
    list-style: square;
    color: #fff;
    font-size: 1.2rem;
  }
}
</style>
