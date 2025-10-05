<script lang="ts" setup>
import HeaderWidhet from '@/components/HeaderWidhet.vue'
import AboutWidget from '@/components/AboutWidget.vue'
import ProsWidget from '@/components/ProsWidget.vue'
</script>

<template>
  <HeaderWidhet></HeaderWidhet>
  <main class="main">
    <AboutWidget></AboutWidget>
    <ProsWidget></ProsWidget>
  </main>
</template>

<style lang="scss" scoped>
.main {
  margin-left: 142px;
}
</style>
