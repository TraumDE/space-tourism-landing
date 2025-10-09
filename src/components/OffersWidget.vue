<script lang="ts" setup>
import { ref } from 'vue'

import OfferCardItem from './OfferCardItem.vue'

import type { OfferCard } from '@/types'

const offerCards = ref<OfferCard[]>([
  {
    title: 'Suborbital Flight',
    price: 500000,
    image: '/images/offer-1.webp',
    time: {
      value: 1,
      timeUnit: 'hour',
    },
  },
  {
    title: 'Orbital Adventure',
    price: 2000000,
    image: '/images/offer-2.webp',
    time: {
      value: 3,
      timeUnit: 'days',
    },
  },
  {
    title: 'Moon Landing',
    price: 5000000,
    image: '/images/offer-3.webp',
    time: {
      value: 7,
      timeUnit: 'days',
    },
  },
  {
    title: 'Suborbital Flight',
    image: '/images/offer-4.webp',
    price: 9000000,
    time: {
      value: 8,
      timeUnit: 'days',
    },
  },
  {
    title: 'Comet Chase Expedition',
    price: 12000000,
    image: '/images/offer-5.webp',
    time: {
      value: 12,
      timeUnit: 'days',
    },
  },
])
</script>

<template>
  <section class="offers">
    <h2 class="offers__title">
      <p class="offers__kicker">BEST OFFERS</p>
      Explore Our Cosmic Adventures
    </h2>
    <div class="offers__cards">
      <OfferCardItem
        v-for="card in offerCards"
        :key="card.title"
        :title="card.title"
        :price="card.price"
        :image="card.image"
        :time="card.time"
      ></OfferCardItem>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>
