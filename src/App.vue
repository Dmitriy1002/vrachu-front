<script setup>
import { RouterLink, RouterView } from 'vue-router'
import TheHeader from './components/TheHeader.vue'
import TheFooter from './components/TheFooter.vue'
</script>

<template>
  <header>
    <TheHeader></TheHeader>
  </header>

  <RouterView />
  <TheFooter></TheFooter>
</template>

<style scoped></style>
