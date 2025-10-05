<script lang="ts" setup>
import AccentButton from './AccentButton.vue'
import AppLogoIcon from './icons/AppLogoIcon.vue'
import { RouterLink } from 'vue-router'
</script>

<template>
  <nav id="nav" class="nav">
    <RouterLink to="/" class="nav__logo">
      <AppLogoIcon></AppLogoIcon>
    </RouterLink>
    <div class="nav__main">
      <RouterLink class="nav__link" to="/">Home</RouterLink>
      <RouterLink class="nav__link" to="/">About</RouterLink>
      <RouterLink class="nav__link" to="/">Explore</RouterLink>
      <RouterLink class="nav__link" to="/">Blog</RouterLink>
      <RouterLink class="nav__link" to="/">About Us</RouterLink>
      <RouterLink class="nav__link" to="/">Contact</RouterLink>

      <AccentButton>
        <template #text> Book Trip </template>
      </AccentButton>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
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
    font-family: 'Figtree', sans-serif;
    font-size: 18px;
    font-weight: 700;
    color: var(--main-font-color);
    text-decoration: none;
    transition: text-decoration 0.3s ease-out;

    &:hover {
      text-decoration: underline;
    }
  }
}
</style>
