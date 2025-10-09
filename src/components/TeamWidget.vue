<script lang="ts" setup>
import { ref } from 'vue'

import type { Team } from '@/types'

const team = ref<Team[]>([
  {
    name: 'Zylan Vexor',
    position: 'Galactic Travel Director',
    image: '/tourism-landing/images/team-1.webp',
  },
  {
    name: "Threxis N'alor",
    position: 'Zero Gravity Specialist',
    image: '/tourism-landing/images/team-2.webp',
  },
  {
    name: "Xylozar K'thar",
    position: 'Cosmic Expedition Leader',
    image: '/tourism-landing/images/team-3.webp',
  },
  {
    name: 'Virok Tal’mor',
    position: 'Celestial Events Coordinator',
    image: '/tourism-landing/images/team-4.webp',
  },
  {
    name: "Zarathis Or'dan",
    position: 'Astro-Adventurer Consultant',
    image: '/tourism-landing/images/team-5.webp',
  },
])
</script>

<template>
  <section class="team">
    <h2 class="team__title section-title">The Astronauts of Our Adventure: Meet the Team</h2>
    <div class="team__main">
      <ul class="team__list">
        <li class="team__list-item">All</li>
        <li class="team__list-item" v-for="member in team" :key="member.image">
          {{ member.name }}
        </li>
      </ul>
      <div class="team__cards">
        <figure class="team__card" v-for="member in team" :key="member.image">
          <img :src="member.image" :alt="member.name" />
          <figcaption>
            <h3 class="team__card-name">{{ member.name }}</h3>
            <p class="team__card-position">{{ member.position }}</p>
          </figcaption>
        </figure>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.team {
  padding-top: 142px;

  &__title {
    padding-bottom: 49px;
  }

  &__main {
    display: flex;
    flex-wrap: nowrap;
    align-items: center;
    gap: 40px;
  }

  &__list {
    @include font($size: 20px, $weight: 300);
  }

  &__list-item {
    &:first-child {
      @include font(var(--accent-color), $size: inherit, $weight: 700);

      background: var(--main-gradient);
      background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    line-height: 200%;
    text-wrap: nowrap;
  }

  &__cards {
    display: flex;
    flex-shrink: 0;
    gap: 42px;
    text-align: center;
    overflow-x: scroll;
  }

  &__card-name {
    @include font($weight: 500);

    padding-top: 19px;
  }

  &__card-position {
    @include font($size: 12px, $weight: 500);
  }
}
</style>
