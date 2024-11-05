<template>
  <div>
    <header>
      <navbar v-if="isHomePage" />
      <nav-comp class="company-navbar" v-else />
    </header>
    <main>
      <slot />
    </main>
    <footer>
      <footerpage />
    </footer>
  </div>
</template>

<style scoped>
</style>

<script setup>
import { useRoute } from 'vue-router'

const route = useRoute()

// Check if the current page is the homepage
const isHomePage = computed(() => route.path === '/')
</script>