<template>
  <div class="relative w-full flex items-center justify-center bg-cover bg-center"
    :style="{ backgroundImage: 'url(/home-bg.png)' }">
    <!-- Solid overlay to dim the background -->
    <div class="absolute inset-0 bg-black opacity-60"></div>

    <!-- Content -->
    <div class="relative z-10 text-center text-white py-8 md:py-20">
      <h1 class="text-5xl md:text-7xl font-bold mb-6 drop-shadow-lg">SIMURGH: COMING NOV&nbsp;2024</h1>
      <p class="text-lg md:text-2xl max-w-2xl mx-auto">
        Step into the streets in this intense beat-em-up adventure. Play as a fearless woman challenging the status quo,
        fighting for her right to live freely. Prepare to battle through a world where courage is the ultimate weapon.
      </p>
    </div>
  </div>
</template>