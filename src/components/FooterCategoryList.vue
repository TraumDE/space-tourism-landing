<script lang="ts" setup>
import { RouterLink } from 'vue-router'

import type { Link } from '@/types'

interface Props {
  links: Link[]
}

const props = defineProps<Props>()
</script>

<template>
  <section class="footer__category">
    <h3 class="footer__category-title">
      <slot name="title"></slot>
    </h3>
    <ul class="footer__category-list">
      <li v-for="link in props.links" :key="link.link" class="footer__category-item">
        <RouterLink :to="link.link">
          {{ link.title }}
        </RouterLink>
      </li>
    </ul>
  </section>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.footer__category {
  display: flex;
  flex-direction: column;

  &-title {
    @include font(var(--accent-color), 19px, 700);

    padding-bottom: 19px;
    text-transform: capitalize;
  }

  &-list {
    @include font($size: 15px, $weight: 400);

    text-transform: capitalize;
    display: flex;
    flex-direction: column;
    gap: 13px;
  }
}
</style>
