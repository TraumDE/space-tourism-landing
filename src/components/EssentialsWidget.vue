<script lang="ts" setup>
import { ref } from 'vue'

import EssentialsCard from './EssentialsItem.vue'

import type { EssentialsItem } from '@/types'

const essentials = ref<EssentialsItem[]>([
  {
    title: 'Choose Your Space Adventure!',
    description:
      'Forem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eu turpis molestie, dictum est a, mattis tellus. Sed dignissim, metus nec fringilla accumsan, risus sem sollicitudin lacus, ut interdum tellus elit sed risus. Maecenas eget condimentum velit, sit amet feugiat lectus. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Praesent auctor purus luctus enim egestas, ac scelerisque ante pulvinar. Donec ut rhoncus ex. ',
    image: '/tourism-landing/images/cosmonaut-1.webp',
  },
  {
    title: 'Prepare for Launch!',
    description:
      'Porem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eu turpis molestie, dictum est a, mattis tellus. Sed dignissim, metus nec fringilla accumsan, risus sem sollicitudin lacus, ut interdum tellus elit sed risus. Maecenas eget condimentum velit, sit amet feugiat lectus. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
    image: '/tourism-landing/images/cosmonaut-2.webp',
  },
  {
    title: 'Blast Off and Explore the Cosmos',
    description:
      'Porem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eu turpis molestie, dictum est a, mattis tellus. Sed dignissim, metus nec fringilla accumsan, risus sem sollicitudin lacus, ut interdum tellus elit sed risus. Maecenas eget condimentum velit, sit amet feugiat lectus. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
    image: '/tourism-landing/images/cosmonaut-3.webp',
  },
])
</script>
<template>
  <section class="essentials">
    <EssentialsCard
      v-for="(essential, index) in essentials"
      :key="index"
      :id="index"
      :title="essential.title"
      :image="essential.image"
      :description="essential.description"
    ></EssentialsCard>
  </section>
</template>
<style lang="scss" scoped>
.essentials {
  padding-top: 120px;
  display: flex;
  gap: 44px;
  flex-direction: column;
}
</style>
