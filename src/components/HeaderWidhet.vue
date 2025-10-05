<script lang="ts" setup>
import AccentButton from './AccentButton.vue'
import ArrowsDownIcon from './icons/ArrowsDownIcon.vue'
</script>

<template>
  <header id="header" class="header">
    <h1 class="header__title">Travel Beyond Earth</h1>
    <img class="header__image" src="/images/astronaut.webp" alt="Astronaut" />
    <div class="header__separate"></div>
    <AccentButton>
      <template #text>Get Started</template>
      <template #icon>
        <ArrowsDownIcon></ArrowsDownIcon>
      </template>
    </AccentButton>
  </header>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.header {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-top: 39px;
  padding-bottom: 21px;

  &__title {
    @include font($size: 80px, $weight: 900);
    letter-spacing: -2%;
    line-height: 65%;
  }

  &__separate {
    position: absolute;
    bottom: 0;
    width: 100vw;
    height: 1px;
    border: 1px dashed #747474;
  }
}
</style>
