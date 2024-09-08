<template>
  <div class="main">
    <NuxtRouteAnnouncer />
    <NuxtLoadingIndicator />
    <!-- <NuxtWelcome /> -->
    <div class="flex flex-col min-h-screen p-4 border-t border-yellow-300">
      <AppHeader />
      <main class="flex-grow">
        <NuxtPage />
      </main>
      <AppFooter />
    </div>
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
  /* padding: 16px; */
  background: #0c0f1b;
  /* min-height: 100vh; */
  
}
</style>