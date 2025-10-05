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
  <a href="/">
    <TwitterIcon v-if="props.icon === 'twitter'"></TwitterIcon>
    <FacebookIcon v-else-if="props.icon === 'facebook'"></FacebookIcon>
    <LinkedinIcon v-else-if="props.icon === 'linkedin'"></LinkedinIcon>
  </a>
</template>
