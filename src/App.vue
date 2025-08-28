<script setup lang="ts">
import Banner from './components/ui/Banner.vue';
import Header from './components/sections/Header.vue';
import Services from './components/sections/Services.vue';
import News from './components/sections/News.vue';
import Footer from './components/sections/Footer.vue';
</script>

<template>
  <Header />
  <Banner />
  <Services />
  <News/>
  <Footer/>
  <main id="content">
    <RouterView />
  </main>
</template>

<style scoped></style>
