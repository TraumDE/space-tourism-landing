<script lang="ts" setup>
import AccentButton from './AccentButton.vue'
import ArrowsDownIcon from './icons/ArrowsDownIcon.vue'
import SocialIcon from './SocialIcon.vue'
</script>

<template>
  <header id="header" class="header">
    <div class="header__socials">
      <SocialIcon icon="twitter"></SocialIcon>
      <SocialIcon icon="facebook"></SocialIcon>
      <SocialIcon icon="linkedin"></SocialIcon>
    </div>
    <h1 class="header__title">Travel Beyond Earth</h1>
    <img class="header__image" src="/images/astronaut.webp" alt="Astronaut" />
    <AccentButton>
      <template #text>Get Started</template>
      <template #icon>
        <ArrowsDownIcon></ArrowsDownIcon>
      </template>
    </AccentButton>
    <div class="header__separate"></div>
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

  &__socials {
    position: absolute;
    right: 82px;
    display: flex;
    flex-direction: column;
    gap: 17px;
    padding-block: 14px;
  }

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
