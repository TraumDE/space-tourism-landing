<script lang="ts" setup></script>

<template>
  <button class="button">
    <slot name="text">Button text</slot>
    <slot name="icon"></slot>
  </button>
</template>

<style lang="scss" scoped>
.button {
  font-family: 'Figtree';
  font-weight: 600;
  font-size: 15px;
  padding-block: 13px;
  padding-inline: 34px;
  border-radius: 50vh;
  border: none;
  color: var(--main-font-color);
  background: var(--main-gradient);
  transition: box-shadow 0.3s ease-out;

  &:hover {
    box-shadow:
      inset 0 0 30px 0 rgba(255, 255, 255, 0.3),
      0 20px 30px 0 rgba(64, 100, 228, 0.3),
      -20px -20px 50px 0 rgba(42, 94, 142, 0.5),
      10px 20px 80px 0 rgba(122, 33, 237, 0.3);
  }
}
</style>
