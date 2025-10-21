<script lang="ts" setup>
import formatBasePath from '@/utils/formatBasePath'

import type { OfferCard } from '@/types'

const props = defineProps<OfferCard>()

const formatPrice = (price: number): string => {
  const userLocale: string = navigator.language
  const formatter: Intl.NumberFormat = new Intl.NumberFormat(userLocale, {
    style: 'currency',
    currency: 'USD',
    maximumFractionDigits: 0,
  })

  return formatter.format(price)
}
</script>

<template>
  <div :style="{ 'background-image': `url(${formatBasePath(props.image)})` }" class="offers__card">
    <h3>
      <span class="offers__card-title">{{ props.title }}</span>
      <span class="offers__card-price">
        {{ formatPrice(props.price) }}
        <span class="offers__card-length">{{ props.time.value }} {{ props.time.timeUnit }}</span>
      </span>
    </h3>
  </div>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.offers__card {
  min-height: 360px;
  background-repeat: no-repeat;
  background-size: cover;
  border-radius: 22px;
  box-shadow: inset 0 -120px 0 0 rgb(0 0 0 / 60%);
  display: flex;
  padding-left: 28px;
  background-position: center;
  flex-direction: column;
  align-items: start;
  justify-content: end;
  transition:
    filter 0.5s ease-out,
    background-position 0.5s ease-out;

  &:hover {
    filter: brightness(1.5);
    background-position: 0 0;
  }

  &-title {
    @include font($size: 20px, $weight: 700);
  }

  &-price {
    @include font($size: 36px, $weight: 700);

    display: flex;
    align-items: self-end;
    gap: 12px;
  }

  &-length {
    @include font(var(--accent-color), $weight: 700);
  }
}
</style>
