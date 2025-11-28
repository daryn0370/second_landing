<script setup>
import Header from './components/Header.vue';
import HomePage from './components/HomePage.vue';
import Info from './components/Info.vue';
import Market from './components/Market.vue';
import Pros from './components/Pros.vue';
import Plan from './components/Plan.vue';
import Referral from './components/Referral.vue';
import Footer from './components/footer.vue';
</script>

<template>
  <div class="page">
    <Header />
    <HomePage />
    <Info />
    <Market />
    <Pros />
    <Plan />
    <Referral />
    <Footer />
  </div>
</template>

<style scoped>
:global(body) {
  margin: 0;
  background: #2b2b3d;
  overflow-x: hidden;
}

:global(#app) {
  min-height: 100vh;
  background: #2b2b3d;
}

.page {
  min-height: 100vh;
  background: #2b2b3d;
  font-family: 'Segoe UI', Arial, sans-serif;
}
</style>
