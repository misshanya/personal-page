<script setup lang="ts">
import Hi from './components/Hi.vue';
import AboutMe from './components/AboutMe.vue';
import Projects from './components/Projects.vue';
</script>

<template>
  <main class="snap-container">
    <section class="snap-section"><Hi/></section>
    <section class="snap-section"><AboutMe/></section>
    <section class="snap-section"><Projects/></section>
  </main>
</template>

<style scoped>
.snap-container {
  height: 100vh;
  overflow-y: scroll;
  scroll-snap-type: y mandatory;

  -webkit-overflow-scrolling: touch;
}

.snap-section {
  height: 100vh;
  scroll-snap-align: start;
}
</style>
