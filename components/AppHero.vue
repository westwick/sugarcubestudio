<script setup>
import heroImage from "@/assets/images/homepagetest.png";
</script>

<template>
  <div
    class="hero relative w-full flex items-center bg-cover bg-center min-h-[600px]"
    :style="{ backgroundImage: `url(${heroImage})` }"
  >
    <!-- Solid overlay to dim the background -->
    <div class="absolute inset-0 bg-black opacity-40"></div>

    <!-- Content -->
    <div class="relative z-10 text-white py-48 px-8 container mx-auto">
      <div class="md:w-1/2 text-center md:text-left">
        <h1 class="text-3xl md:text-5xl font-bold drop-shadow-lg mt-2 mb-4">
          Simurgh: Coming Soon
        </h1>
        <p
          class="text-lg md:text-2xl max-w-2xl md:max-w-none mx-auto font-medium text-slate-300"
        >
          In a game where myth, history and reality intertwine, step into the
          role of a fearless woman battling a corrupt status quo for her right
          to live freely. Embark on an epic fight for freedom that will shape
          the destiny of a nation!
        </p>
        <NuxtLink
          to="/apps/simurgh"
          class="hero-button-main gradient-button-yellow"
        >
          Learn More</NuxtLink
        >
      </div>
    </div>
  </div>
</template>

<style>
.hero {
  background-position-y: 0;
}
.hero-button-main {
  @apply mt-6 relative inline-block text-base sm:text-xl py-2 px-6 sm:py-3 md:px-10 cursor-pointer text-black font-bold rounded-md;
}
</style>
