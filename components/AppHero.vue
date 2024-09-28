<template>
  <div
    class="relative w-full flex items-center justify-center bg-cover bg-center"
    :style="{ backgroundImage: 'url(/bird.jpg)' }"
  >
    <!-- Solid overlay to dim the background -->
    <div class="absolute inset-0 bg-black opacity-40"></div>

    <!-- Content -->
    <div class="relative z-10 text-center text-white py-8 md:py-20 px-4">
      <h1 class="text-5xl md:text-7xl font-bold mb-6 drop-shadow-lg mt-40">
        Simurgh: Coming Soon
      </h1>
      <p
        class="text-lg md:text-2xl max-w-2xl mx-auto font-medium text-slate-300"
      >
        Step into the streets in this intense beat-em-up adventure. Play as a
        fearless woman challenging the status quo, fighting for her right to
        live freely.
      </p>
      <NuxtLink to="/apps" class="hero-button-main gradient-button-yellow">
        Learn More</NuxtLink
      >
    </div>
  </div>
</template>

<style>
.hero-button-main {
  @apply mt-6 relative inline-block text-base sm:text-xl py-2 px-6 sm:py-3 md:px-10 cursor-pointer text-black font-bold rounded-md;
}
</style>
