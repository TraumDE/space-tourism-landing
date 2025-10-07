<script lang="ts" setup>
import PlayIcon from './icons/PlayIcon.vue'

import type { VideoCard } from '@/types/videoCard'

const props = defineProps<VideoCard>()
</script>

<template>
  <div class="guide__card">
    <div
      :style="{ 'background-image': `url(/tourism-landing${props.image})` }"
      class="guide__card-main"
    >
      <button class="guide__card-play">
        <PlayIcon></PlayIcon>
      </button>
      <span class="guide__card-time"> {{ props.length / 60 }} min </span>
    </div>
    <h3 class="guide__card-title">
      {{ props.title }}
    </h3>
    <sub class="guide__card-description">
      {{ props.description }}
    </sub>
  </div>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.guide__card {
  width: 100%;

  &-main {
    display: flex;
    justify-content: space-between;
    padding: 26px;
    align-items: end;
    width: 100%;
    max-width: 1149px;
    height: 250px;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    background-color: #98989a;
    border-radius: 9px;

    box-shadow: inset 0 -80px 80px 0 #000000;
  }

  &-play {
    background: transparent;
    border: none;
  }

  &-time {
    @include font(#7e7e81, 13px, 400);
  }

  &-title {
    @include font($size: 17px, $weight: 600);
  }

  &-description {
    @include font(#98989a, 13px, 400);
  }
}
</style>
