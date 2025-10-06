<script lang="ts" setup>
import HeaderWidhet from '@/components/HeaderWidhet.vue'
import AboutWidget from '@/components/AboutWidget.vue'
import ProsWidget from '@/components/ProsWidget.vue'
import BookWidget from '@/components/BookWidget.vue'
</script>

<template>
  <HeaderWidhet></HeaderWidhet>
  <main class="main">
    <AboutWidget></AboutWidget>
    <ProsWidget></ProsWidget>
    <BookWidget></BookWidget>
  </main>
</template>

<style lang="scss" scoped>
.main {
  margin-left: 142px;
}
</style>
