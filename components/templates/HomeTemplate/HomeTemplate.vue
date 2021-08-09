<template>
  <div class="home-template">
    <Container>
      <form @submit.prevent="onSubmit">
        <Input v-model="text" placeholder="First name" />
        <Button text="Go" type="submit" />
      </form>

      <List v-show="items.length >= 1" :items="items" />
    </Container>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import faker from 'faker'

export default Vue.extend({
  name: 'HomeTemplate',
  data() {
    return {
      text: '',
      items: [] as string[],
      resultLimit: 5
    }
  },
  methods: {
    onSubmit() {
      while (this.items.length < this.resultLimit) {
        this.items.push(`${this.text} ${faker.name.lastName()}`)
      }
    }
  }
})
</script>

<style lang="scss" scoped>
.home-template {
  height: 100%;
  width: 100%;
  display: grid;
  justify-content: center;
  align-content: center;
}
</style>
