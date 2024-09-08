<template>
  <div class="relative w-full flex items-center justify-center bg-cover bg-center"
    :style="{ backgroundImage: 'url(/home-bg.png)' }">
    <!-- Solid overlay to dim the background -->
    <div class="absolute inset-0 bg-black opacity-70"></div>

    <!-- Content -->
    <div class="relative z-10 text-center text-white py-8 md:py-20 px-4">
      <h1 class="text-5xl md:text-7xl font-bold mb-6 drop-shadow-lg">Simurgh: Coming Soon</h1>
      <p class="text-lg md:text-2xl max-w-2xl mx-auto font-medium text-slate-300">
        Step into the streets in this intense beat-em-up adventure. Play as a fearless woman challenging the status quo,
        fighting for her right to live freely.
      </p>
      <NuxtLink to="/apps"
        class="mt-6 relative inline-block text-md sm:text-xl py-2 px-4 sm:py-3 sm:px-6 cursor-pointer text-white border-2 border-transparent rounded-md gradient-border">
        Learn More</NuxtLink>
    </div>
  </div>
</template>

<style>
.gradient-border {
  background-color: hsla(0, 0%, 8%, .3);
  -webkit-backdrop-filter: blur(10px);
  backdrop-filter: blur(10px);
  border-radius: .5rem;
  position: relative;
  border: 1px solid #ccc;
  color: #fff;
  transition: all 0.4s ease-in-out;
}

.gradient-border:hover {
  border: 1px solid yellow;
  color: yellow;
}
</style>