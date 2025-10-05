<script lang="ts" setup>
import NavWidget from '@/components/NavWidget.vue'
import FooterWidget from '@/components/FooterWidget.vue'
</script>

<template>
  <NavWidget></NavWidget>
  <slot></slot>
  <FooterWidget></FooterWidget>
</template>
