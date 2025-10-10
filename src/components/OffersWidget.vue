<script lang="ts" setup>
import { ref } from 'vue'

import OfferCardItem from './OfferCardItem.vue'

import type { OfferCard } from '@/types'

const offerCards = ref<OfferCard[]>([
  {
    title: 'Suborbital Flight',
    price: 500000,
    image: '/tourism-landing/images/offer-1.webp',
    time: {
      value: 1,
      timeUnit: 'hour',
    },
  },
  {
    title: 'Orbital Adventure',
    price: 2000000,
    image: '/tourism-landing/images/offer-2.webp',
    time: {
      value: 3,
      timeUnit: 'days',
    },
  },
  {
    title: 'Moon Landing',
    price: 5000000,
    image: '/tourism-landing/images/offer-3.webp',
    time: {
      value: 7,
      timeUnit: 'days',
    },
  },
  {
    title: 'Suborbital Flight',
    image: '/tourism-landing/images/offer-4.webp',
    price: 9000000,
    time: {
      value: 8,
      timeUnit: 'days',
    },
  },
  {
    title: 'Comet Chase Expedition',
    price: 12000000,
    image: '/tourism-landing/images/offer-5.webp',
    time: {
      value: 12,
      timeUnit: 'days',
    },
  },
])
</script>

<template>
  <section class="offers">
    <h2 class="offers__title section-title">
      <p class="offers__kicker">BEST OFFERS</p>
      Explore Our Cosmic Adventures
    </h2>
    <div class="offers__cards">
      <OfferCardItem
        v-for="(card, index) in offerCards"
        :key="card.title"
        :title="card.title"
        :price="card.price"
        :image="card.image"
        :time="card.time"
        :class="`offers__card--item${index}`"
      ></OfferCardItem>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.offers {
  padding-top: 120px;
  &__kicker {
    @include gradient-font($size: 20px, $weight: 500);
  }

  &__cards {
    display: grid;
    grid-template-columns: repeat(9, 1fr);
    grid-template-rows: repeat(6, 1fr);
    gap: 30px;
    max-width: 1140px;
  }

  &__card--item0 {
    grid-column: span 6 / span 6;
    grid-row: span 3 / span 3;
  }

  &__card--item1 {
    grid-column: span 3 / span 3;
    grid-row: span 3 / span 3;
    grid-column-start: 7;
  }

  &__card--item2 {
    grid-column: span 3 / span 3;
    grid-row: span 3 / span 3;
    grid-row-start: 4;
  }

  &__card--item3 {
    grid-column: span 3 / span 3;
    grid-row: span 3 / span 3;
    grid-column-start: 4;
    grid-row-start: 4;
  }

  &__card--item4 {
    grid-column: span 3 / span 3;
    grid-row: span 3 / span 3;
    grid-column-start: 7;
    grid-row-start: 4;
  }
}
</style>
