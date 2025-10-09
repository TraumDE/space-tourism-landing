<script lang="ts" setup>
import SecondaryButton from './SecondaryButton.vue'
import AccentButton from './AccentButton.vue'
</script>

<template>
  <section class="about">
    <div class="about__planets">
      <img class="about__planets-planet-1" src="/images/planet-1.webp" alt="planet" />
      <img class="about__planets-planet-2" src="/images/earth.webp" alt="earth planet one" />
      <img class="about__planets-planet-3" src="/images/planet-2.webp" alt="earth planet two" />
    </div>
    <div class="about__main">
      <h2 class="about__title">Take Off Into The Stars</h2>
      <p class="about__text">
        Forem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eu turpis molestie, dictum
        est a, mattis tellus. Sed dignissim, metus nec fringilla accumsan, risus sem sollicitudin
        lacus, ut interdum tellus elit sed risus. Maecenas eget condimentum velit, sit amet feugiat
        lectus. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos
        himenaeos. Praesent auctor purus luctus enim egestas, ac scelerisque ante pulvinar. Donec ut
        rhoncus ex. Suspendisse ac rhoncus nisl, eu tempor urna. Curabitur vel bibendum lorem.
      </p>
      <div class="about__buttons">
        <SecondaryButton>
          <template #text>Details</template>
        </SecondaryButton>
        <AccentButton>
          <template #text>Launch</template>
        </AccentButton>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.about {
  position: relative;
  padding-top: 247px;

  &__title {
    @include font($size: 50px, $weight: 300);

    padding-bottom: 26px;
  }

  &__text {
    @include font($size: 16px, $weight: 400);

    max-width: 679px;
    padding-bottom: 36px;
  }

  &__buttons {
    display: flex;
    flex-direction: row;
    gap: 30px;
  }

  &__planets {
    position: relative;
    background-color: rgb(255 11 11);

    & * {
      position: absolute;
    }

    &-planet-1 {
      right: 139px;
      transition: transform ease-in-out 1s;

      &:hover {
        transform: rotate(45deg);
      }
    }

    &-planet-2 {
      right: 0;
      transition: right ease-in-out 1s;

      &:hover {
        right: -20px;
      }
    }

    &-planet-3 {
      right: 145px;
      top: 366px;
      transition: transform ease-in-out 1s;

      &:hover {
        transform: rotate(15deg);
      }
    }
  }
}
</style>
