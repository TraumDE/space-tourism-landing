<script lang="ts" setup>
import { ref } from 'vue'
import AppLogo from './AppLogo.vue'
import FooterCategoryList from './FooterCategoryList.vue'

import type { Link } from '@/types'

const moreOnTheBlogLinks = ref<Link[]>([
  {
    link: '/',
    title: 'About Cosmic Tourism',
  },
  {
    link: '/',
    title: 'Contributors & Writers',
  },
  {
    link: '/',
    title: 'Write For Us',
  },
  {
    link: '/',
    title: 'Contact Us',
  },
  {
    link: '/',
    title: 'Privacy Policy',
  },
])

const moreOnCosmicTourismLinks = ref<Link[]>([
  {
    link: '/',
    title: 'The Team',
  },
  {
    link: '/',
    title: 'Jobs',
  },
  {
    link: '/',
    title: 'Press',
  },
])
</script>

<template>
  <footer id="footer" class="footer">
    <div class="footer__left">
      <div class="footer__logo-container">
        <AppLogo></AppLogo>
        <p class="footer__logo-subtext">Get out there & discover your next cosmic journey!</p>
      </div>
      <p class="footer__copyright">Copyright 2025 Cosmic Tourism, Inc. Terms & Privacy</p>
    </div>
    <div class="footer__right">
      <FooterCategoryList :links="moreOnTheBlogLinks">
        <template #title>More on The Blog</template>
      </FooterCategoryList>
      <FooterCategoryList :links="moreOnCosmicTourismLinks">
        <template #title>More on Cosmic Tourism</template>
      </FooterCategoryList>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use '@/assets/styles/helpers' as *;

.footer {
  display: flex;
  justify-content: space-around;
  padding-top: 210px;
  padding-bottom: 83px;

  &__left {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  &__right {
    display: flex;
    flex-direction: row;
    gap: 185px;
  }

  &__logo-subtext {
    @include font($size: 15px, $weight: 700);
  }

  &__copyright {
    @include font($size: 15px, $weight: 400);
  }
}
</style>
