<script lang="ts" setup>
import SpiralIcon from './icons/SpiralIcon.vue'
import LandsIcon from './icons/LandsIcon.vue'
import SafetyIcon from './icons/SafetyIcon.vue'
import AstronautIcon from './icons/AstronautIcon.vue'
</script>

<template>
  <section class="pros">
    <div class="pros__card">
      <AstronautIcon class="pros__card-icon"></AstronautIcon>
      <h3 class="pros__card-title">Expert Astronauts</h3>
      <p class="pros__card-description">Jorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </div>
    <div class="pros__card">
      <LandsIcon class="pros__card-icon"></LandsIcon>
      <h3 class="pros__card-title">Personalized Adventures</h3>
      <p class="pros__card-description">Corem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </div>
    <div class="pros__card">
      <SpiralIcon class="pros__card-icon"></SpiralIcon>
      <h3 class="pros__card-title">Zero Gravity Fun</h3>
      <p class="pros__card-description">Dorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </div>
    <div class="pros__card">
      <SafetyIcon class="pros__card-icon"></SafetyIcon>
      <h3 class="pros__card-title">Unmatched Safety</h3>
      <p class="pros__card-description">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.pros {
  padding-top: 150px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding-inline: 87px;
  gap: 120px;

  &__card {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  &__card-title {
    @include font($size: 18px, $weight: 400);
    max-width: 163px;
    padding-top: 15px;
  }

  &__card-description {
    @include font($size: 12px, $weight: 400);
    max-width: 163px;
  }

  &__card-icon {
    transition: filter 0.3s ease-out;

    &:hover {
      filter: drop-shadow(0 4px 50px rgba(2, 93, 113, 0.7))
        drop-shadow(0 20px 105.2px rgba(29, 53, 139, 0.6))
        drop-shadow(-20px -20px 60.2px rgba(42, 94, 142, 0.8))
        drop-shadow(10px 20px 84px rgba(122, 33, 237, 0.3));
    }
  }
}
</style>
