<script lang="ts" setup></script>

<template>
  <button class="button">
    <slot name="text">Button text</slot>
    <slot name="icon"></slot>
  </button>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.button {
  @include font(var(--accent-color), 15px, 600);

  padding-block: 13px;
  padding-inline: 34px;
  border-radius: 50vh;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 13px;
  border: 2px solid var(--accent-color);
  background-color: transparent;
  transition: box-shadow 0.3s ease-out;
}
</style>
