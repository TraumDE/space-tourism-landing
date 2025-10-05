<script lang="ts" setup>
import HeaderWidhet from '@/components/HeaderWidhet.vue'
import AboutWidget from '@/components/AboutWidget.vue'
</script>

<template>
  <HeaderWidhet></HeaderWidhet>
  <main class="main">
    <AboutWidget></AboutWidget>
  </main>
</template>

<style lang="scss" scoped>
.main {
  margin-left: 142px;
}
</style>
