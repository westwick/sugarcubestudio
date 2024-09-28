<template>
  <div class="main">
    <NuxtRouteAnnouncer />
    <NuxtLoadingIndicator />
    <!-- <NuxtWelcome /> -->
    <div
      class="flex flex-col min-h-screen p-0 md:p-4 border-t border-yellow-300"
    >
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
    return titleChunk
      ? `${titleChunk} - Sugar Cube Studio`
      : "Sugar Cube Studio";
  },
});
</script>

<style>
body {
  font-family: "Figtree", sans-serif;
  background: #171926;
  color: #fff;
}

.main {
  /* padding: 16px; */
  background: #0c0f1b;
  /* min-height: 100vh; */
}
.gradient-button {
  background: linear-gradient(to right, #525fb1, #5cb7e0);
  transition: all 0.3s ease;
}

.gradient-button:hover {
  background: linear-gradient(to right, #4a56a0, #4da5cc);
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.gradient-button-yellow {
  background: linear-gradient(to right, #f9b857, #fce680);
}

.gradient-button-yellow:hover {
  background: linear-gradient(to right, #e0a64e, #e3cd73);
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
</style>
