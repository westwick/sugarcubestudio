<template>
  <div
    class="relative w-full flex items-center justify-center bg-cover bg-center"
    :style="{ backgroundImage: 'url(/bird.jpg)' }"
  >
    <!-- Solid overlay to dim the background -->
    <div class="absolute inset-0 bg-black opacity-40"></div>

    <!-- Content -->
    <div class="relative z-10 text-center text-white py-4 px-4">
      <h1 class="text-5xl md:text-7xl font-bold drop-shadow-lg mt-2 mb-80">
        Simurgh: Coming Soon
      </h1>
      <p
        class="text-lg md:text-2xl max-w-2xl mx-auto font-medium text-slate-300"
      >
        In a game where myth, history and reality intertwine, step into the role
        of a fearless woman battling a corrupt status quo for her right to live
        freely. Embark on an epic fight for freedom that will shape the destiny
        of a nation!
      </p>
      <NuxtLink
        to="/apps/simurgh"
        class="hero-button-main gradient-button-yellow"
      >
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
