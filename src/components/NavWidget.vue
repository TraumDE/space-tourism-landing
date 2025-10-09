<script lang="ts" setup>
import { RouterLink } from 'vue-router'

import AppLogo from './AppLogo.vue'
import SearchIcon from './icons/SearchIcon.vue'
import AccentButton from './AccentButton.vue'
</script>

<template>
  <nav id="nav" class="nav">
    <AppLogo></AppLogo>
    <div class="nav__main">
      <RouterLink class="nav__link" to="/">Home</RouterLink>
      <RouterLink class="nav__link" to="/">About</RouterLink>
      <RouterLink class="nav__link" to="/">Explore</RouterLink>
      <RouterLink class="nav__link" to="/">Blog</RouterLink>
      <RouterLink class="nav__link" to="/">About Us</RouterLink>
      <RouterLink class="nav__link" to="/">Contact</RouterLink>
      <SearchIcon role="button" tabindex="0"></SearchIcon>
      <AccentButton>
        <template #text> Book Trip </template>
      </AccentButton>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.nav {
  padding-top: 24px;
  display: flex;
  flex-direction: row;
  justify-content: space-around;

  &__main {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 26px;
  }

  &__link {
    @include font($size: 18px, $weight: 600);


  }
}
</style>
