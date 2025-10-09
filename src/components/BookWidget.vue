<script lang="ts" setup>
import AccentButton from './AccentButton.vue'

const handleFormSubmit = (): void => {}
</script>

<template>
  <section class="book">
    <form class="book__form">
      <h2 class="book__title section-title">Book Your Cosmic Journey Now</h2>
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

    <div class="book__moon">
      <img class="book__moon-image" src="/images/moon.webp" alt="moon image" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.book {
  padding-top: 160px;
  display: flex;
  flex-direction: row;
  justify-content: space-around;

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
    @include font($size: 16px, $weight: 500);

    background-color: transparent;
    outline: none;
    border: 1px solid #aeaeae;
    border-radius: 999px;
    padding-block: 13px;
    padding-inline: 17px;
    width: 100%;

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

  &__moon {
    filter: drop-shadow(0 20px 30px rgb(64 100 228 / 30%))
      drop-shadow(-20px -20px 50px rgb(42 94 142 / 50%))
      drop-shadow(122px 33px 237px rgb(122 33 237 / 30%));
    display: flex;
    align-items: center;
    transition: transform 1.5s ease-out;

    &:hover {
      transform: rotate(-45deg);
    }
  }
}
</style>
