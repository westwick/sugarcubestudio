<template>
  <div class="main">
    <NuxtRouteAnnouncer />
    <NuxtLoadingIndicator />
    <!-- <NuxtWelcome /> -->
    <AppHeader />
    <NuxtPage />
  </div>
</template>

<script setup lang="ts">
useHead({
  titleTemplate: (titleChunk) => {
    return titleChunk ? `${titleChunk} - Sugar Cube Studio` : 'Sugar Cube Studio';
  }
})
</script>

<style>
body {
  font-family: 'Figtree', sans-serif;
  background: #171926;
  color: #fff;
}
.main {
  padding: 16px;
  background: #0c0f1b;
  min-height: 100vh;
  border-top: 1px solid yellow;
}
</style>