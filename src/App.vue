<script setup>
import { RouterLink, RouterView } from 'vue-router'
import NavBarView from './views/NavBarView.vue';
import Footer from './components/custom/Footer.vue';
</script>

<template>
  <header>
    <div class="wrapper">
      <NavBarView />
    </div>
  </header>
  <RouterView />
  <Footer />
</template>

<style scoped></style>
