<script lang="ts" setup>
import type { OfferCard } from '@/types'

const props = defineProps<OfferCard>()
</script>

<template>
  <div :style="{ 'background-image': `url(${props.image})` }" class="offers__card">
    <h3>
      <span class="offers__card-title">{{ props.title }}</span>
      <span class="offers__card-price">
        $ {{ props.price }}
        <span class="offers__card-length">{{ props.time.value }} {{ props.time.timeUnit }}</span>
      </span>
    </h3>
  </div>
</template>

<style lang="scss" scoped></style>
