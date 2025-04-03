<script setup>
import { RouterLink, RouterView } from 'vue-router'
import NavBarView from './views/NavBarView.vue';
</script>

<template>
  <header>
    <div class="wrapper">
   <NavBarView />
    </div>
  </header>

  <RouterView />
</template>

<style scoped></style>
