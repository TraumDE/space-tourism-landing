<script lang="ts" setup>
import AccentButton from './AccentButton.vue'

const handleFormSubmit = (): void => {}
</script>

<template>
  <section class="book">
    <h2 class="book__title">Book Your Cosmic Journey Now</h2>
    <form class="book__form">
      <fieldset class="book__form-fieldset">
        <legend class="book__form-title">Traveler Details:</legend>
        <input
          class="book__input"
          name="full-name"
          id="full-name"
          type="text"
          placeholder="Full Name"
        />
        <input
          class="book__input"
          name="contact-info"
          id="contact-info"
          type="text"
          placeholder="Contact info"
        />
        <input
          class="book__input"
          name="destination"
          id="destination"
          type="text"
          placeholder="Destination"
        />
        <input
          class="book__input"
          name="passengers"
          id="passengers"
          type="text"
          placeholder="Number of passengers"
        />
        <textarea
          class="book__input book__text-area"
          name="special"
          id="special"
          placeholder="Special Request"
        ></textarea>
        <AccentButton @click.prevent="handleFormSubmit">
          <template #text>Contact Me</template>
        </AccentButton>
      </fieldset>
    </form>
  </section>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.book {
  padding-top: 160px;

  &__title {
    @include font($size: 40px, $weight: 300);
  }

  &__form-title {
    @include font($size: 17px, $weight: 500);
    padding-bottom: 30px;
  }

  &__form {
    padding-top: 24px;
    width: 470px;
  }

  &__form-fieldset {
    display: flex;
    flex-direction: column;
    gap: 20px;
    border: none;
  }

  &__input {
    background-color: transparent;
    outline: none;
    border: 1px solid #aeaeae;
    border-radius: 999px;
    padding-block: 13px;
    padding-inline: 17px;
    width: 100%;

    @include font($size: 16px, $weight: 500);

    &::placeholder {
      @include font(#aeaeae, 16px, 500);
    }
  }

  &__text-area {
    width: 100%;
    height: 90px;
    resize: none;
    border-radius: 35px;
  }
}
</style>
