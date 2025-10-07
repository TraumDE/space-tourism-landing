<script lang="ts" setup>
import { ref } from 'vue'
import GuideVideoCard from './GuideVideoCard.vue'

import type { VideoCard } from '@/types/videoCard'

const videoCards = ref<VideoCard[]>([
  {
    title: 'The Future of Space Tourism: What to Expect',
    description: 'Morem ipsum dolor sit amet, consectetur adipiscing elit.',
    image: '/images/video-card-1.webp',
    length: 150,
  },
  {
    title: 'Top 10 Destinations in the Cosmos You Must Visit',
    description: 'Porem ipsum dolor sit amet, consectetur adipiscing elit.',
    image: '/images/video-card-2.webp',
    length: 270,
  },
  {
    title: 'The Science Behind Space Travel: How We Make It Safe',
    description: 'Morem ipsum dolor sit amet, consectetur adipiscing elit.',
    image: '/images/video-card-3.webp',
    length: 330,
  },
])
</script>

<template>
  <section class="guide">
    <h2 class="guide__title section-title">A Visual Guide to Cosmic Exploration</h2>
    <div class="guide__video-cards">
      <GuideVideoCard
        v-for="videoCard in videoCards"
        :key="videoCard.title"
        :title="videoCard.title"
        :description="videoCard.description"
        :image="videoCard.image"
        :length="videoCard.length"
      ></GuideVideoCard>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.guide {
  padding-top: 120px;

  &__title {
    padding-bottom: 60px;
  }

  &__video-cards {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 50px;
  }
}
</style>
