<script lang="ts" setup>
import SecondaryButton from './SecondaryButton.vue'
import ArrowRightIcon from './icons/ArrowRightIcon.vue'

import type { EssentialsItem } from '@/types'

interface Props extends EssentialsItem {
  id: number
}

const props = defineProps<Props>()
</script>

<template>
  <section class="essentials__section">
    <div class="essentials__section-image-container">
      <img class="essentials__section-image" :src="props.image" alt="" />
    </div>
    <div class="essentials__section-main">
      <span class="essentials__section-number">0{{ props.id + 1 }}</span>
      <h3 class="essentials__section-title section-title">
        <p class="essentials__section-kicker"><span></span>COSMIC ESSENTIALS</p>
        {{ props.title }}
      </h3>
      <p class="essentials__section-description">
        {{ props.description }}
      </p>
      <SecondaryButton>
        <template #text>Read More</template>
        <template #icon>
          <ArrowRightIcon></ArrowRightIcon>
        </template>
      </SecondaryButton>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.essentials__section {
  $b: #{&};

  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-direction: row;
  position: relative;

  &:nth-child(even) {
    flex-direction: row-reverse;
  }

  &-kicker {
    @include gradient-font($size: 15px, $weight: 800);

    display: flex;
    align-items: center;
    flex-flow: row nowrap;
    gap: 20px;

    & span {
      display: inline-block;
      width: 60px;
      height: 2px;
      background: var(--main-gradient);
    }
  }

  &-image {
    transition: 0.5s ease-out;

    &:hover {
      filter: drop-shadow(0 0 30px rgb(255 255 255 / 30%))
        drop-shadow(0 20px 30px rgb(64 100 228 / 30%))
        drop-shadow(-20px -20px 50px rgb(42 94 142 / 50%))
        drop-shadow(10px 20px 80px rgb(122 33 237 / 30%));
    }
  }

  &-main {
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: start;
    gap: 22px;
  }

  &-description {
    max-width: 512px;
  }

  &-number {
    top: -15%;
    left: 40%;
    position: absolute;
    @include font(#ffffff21, 194px, 400);

    #{$b}:nth-child(even) & {
      top: -15%;
      left: 0;
    }
  }
}
</style>
