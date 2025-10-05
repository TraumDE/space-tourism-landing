<script lang="ts" setup>
import AccentButton from './AccentButton.vue'
</script>

<template>
  <nav id="nav" class="nav">
    <AccentButton>
      <template #text> Book Trip </template>
    </AccentButton>
  </nav>
</template>

<style lang="scss" scoped>
.nav {
  padding-top: 24px;
}
</style>
