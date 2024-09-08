<template>
  <div class="container mx-auto text-center">
    <h1 class="text-xl mb-4">Apps!</h1>
    <p class="flex space-x-4 mx-auto">
      <NuxtLink to="/apps/simurgh" class="link">Simurgh</NuxtLink>
      <NuxtLink to="/apps/nowruz" class="link">Nowruz</NuxtLink>
    </p>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Apps'
})
</script>

<style>
.link {
  @apply text-yellow-300;
}
</style>