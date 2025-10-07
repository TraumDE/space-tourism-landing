<script lang="ts" setup>
import HeaderWidhet from '@/components/HeaderWidhet.vue'
import AboutWidget from '@/components/AboutWidget.vue'
import ProsWidget from '@/components/ProsWidget.vue'
import BookWidget from '@/components/BookWidget.vue'
import GuideWidget from '@/components/GuideWidget.vue'
import TeamWidget from '@/components/TeamWidget.vue'
</script>

<template>
  <HeaderWidhet></HeaderWidhet>
  <main class="main">
    <AboutWidget></AboutWidget>
    <ProsWidget></ProsWidget>
    <TeamWidget></TeamWidget>
    <GuideWidget></GuideWidget>
    <BookWidget></BookWidget>
  </main>
</template>

<style lang="scss" scoped>
.main {
  margin-left: 142px;
}
</style>
