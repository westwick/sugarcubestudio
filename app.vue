<template>
  <div>
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