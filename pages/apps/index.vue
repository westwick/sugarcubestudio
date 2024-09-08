<template>
  <div class="container mx-auto">
    <h1>Apps!</h1>
    <p>
      <NuxtLink to="/apps/simurgh">Simurgh</NuxtLink>
      <NuxtLink to="/apps/nowruz">Nowruz</NuxtLink>
    </p>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Apps'
})
</script>