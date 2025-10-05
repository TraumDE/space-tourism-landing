<script lang="ts" setup>
import TwitterIcon from './icons/TwitterIcon.vue'
import FacebookIcon from './icons/FacebookIcon.vue'
import LinkedinIcon from './icons/LinkedinIcon.vue'

interface Props {
  icon: 'twitter' | 'facebook' | 'linkedin'
}

const props = defineProps<Props>()
</script>

<template>
  <a href="#">
    <TwitterIcon class="social-icon" v-if="props.icon === 'twitter'"></TwitterIcon>
    <FacebookIcon class="social-icon" v-else-if="props.icon === 'facebook'"></FacebookIcon>
    <LinkedinIcon class="social-icon" v-else-if="props.icon === 'linkedin'"></LinkedinIcon>
  </a>
</template>

<style lang="scss">
.social-icon {
  & path {
    transition: fill 0.3s ease-out;
  }

  &:hover path {
    fill: var(--accent-color);
  }
}
</style>
