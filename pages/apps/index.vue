<template>
  <div class="container mt-10 mx-auto text-center content-center">
    <!-- <h1 class="text-xl mb-4">Apps!</h1> -->
    <p class="flex pt-100 space-x-4 mx-auto">
      <NuxtLink
        to="/apps/simurgh"
        class="link app-button flex-1 simurgh-link outline-text"
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
  @apply bg-yellow-300 text-black text-2xl px-20 py-40 rounded-md;
}
.simurgh-link {
  background-image: url("/public/home-bg.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  /* Add any other necessary styles */
}

.outline-text {
  /* -webkit-text-stroke: 1px black; Outline width and color */
  color: white; /* Text color */
  text-shadow: 3px 3px 0 #000, -1px -1px 0 #000, 1px -1px 0 #000,
    -1px 1px 0 #000, 1px 1px 0 #000; /*Additional outline effect */
}
</style>
