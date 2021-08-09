<template>
  <div class="container">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
.container {
  width: 400px;
  display: grid;
  justify-items: center;
  grid-gap: 1rem;
}
</style>
