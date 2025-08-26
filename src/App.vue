<script setup lang="ts">
import Banner from './components/ui/Banner.vue';
import Header from './components/layout/Header.vue';
import Services from './components/sections/Services.vue';
</script>

<template>
  <Header />
  <Banner />
  <Services />
  <main id="content">
    <RouterView />
  </main>
</template>

<style scoped></style>
