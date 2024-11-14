<script setup>
import HomepageView from './views/HomepageView.vue'

const isDesktop = window.innerWidth > 1024
const isTablet = window.innerWidth <= 1024 && window.innerWidth > 748
</script>

<template>
  <template v-if="isDesktop">
    <HomepageView />
  </template>
  <template v-else-if="isTablet">This is tablet</template>
  <template v-else> This is mobile </template>
</template>
