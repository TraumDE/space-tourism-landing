<script lang="ts" setup>
import HeaderWidhet from '@/components/HeaderWidhet.vue'
import AboutWidget from '@/components/AboutWidget.vue'
import ProsWidget from '@/components/ProsWidget.vue'
import BookWidget from '@/components/BookWidget.vue'
import GuideWidget from '@/components/GuideWidget.vue'
import TeamWidget from '@/components/TeamWidget.vue'
import OffersWidget from '@/components/OffersWidget.vue'
import EssentialsWidget from '@/components/EssentialsWidget.vue'
</script>

<template>
  <HeaderWidhet></HeaderWidhet>
  <main class="main">
    <AboutWidget></AboutWidget>
    <ProsWidget></ProsWidget>
    <TeamWidget></TeamWidget>
    <OffersWidget></OffersWidget>
    <EssentialsWidget></EssentialsWidget>
    <GuideWidget></GuideWidget>
    <BookWidget></BookWidget>
  </main>
</template>

<style lang="scss" scoped>
.main {
  margin-inline: 120px auto;
}
</style>
