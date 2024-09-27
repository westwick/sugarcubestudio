<template>
  <div class="container mx-auto text-center content-center">
    <h1 class="text-xl mb-4">Apps!</h1>
    <p class="flex pt-100 space-x-4 mx-auto">
      <NuxtLink to="/apps/simurgh" class="link app-button flex-1"
        >Simurgh</NuxtLink
      >
      <NuxtLink to="/apps/nowruz" class="link app-button flex-1"
        >Nowruz</NuxtLink
      >
    </p>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: "Apps",
});
</script>

<style>
.link {
  @apply text-yellow-300;
}

.app-button {
  @apply bg-yellow-300 text-black px-20 py-40 rounded-md;
}
</style>
