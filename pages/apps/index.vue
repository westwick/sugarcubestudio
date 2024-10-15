<template>
  <PageHeader
    subtitle="Our Applications"
    title="Explore our apps, all available on iOS and Android"
  />
  <div class="bg-gradient-to-t from-[rgb(215,223,232)] to-[rgb(244,246,248)]">
    <div class="container py-16 px-4 lg:px-0 mx-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div class="app-card bg-white rounded-lg overflow-hidden shadow-md">
          <NuxtLink to="/apps/simurgh">
            <img
              src="/bird.jpg"
              alt="Simurgh App"
              class="w-full h-56 object-cover"
            />
          </NuxtLink>

          <div class="p-6">
            <h3 class="text-3xl font-bold mb-2 text-black">Simurgh</h3>
            <div class="flex"></div>
            <p class="text-gray-800">
              Step into the streets in this intense beat-em-up adventure.
              Explore ancient sites and play as a fearless woman challenging the
              status quo, fighting for her right to live freely.
            </p>
          </div>
          <div class="bg-gray-100 flex flex-row border-t-2 border-gray-200 p-6">
            <NuxtLink
              to="/apps/simurgh"
              class="text-blue-950 font-semibold py-2 px-6 rounded transition-all duration-500 hover:bg-yellow-400 bg-yellow-300"
            >
              Learn More
            </NuxtLink>
          </div>
        </div>

        <!-- app card -->
        <div class="app-card bg-white rounded-lg overflow-hidden shadow-md">
          <NuxtLink to="/apps/simurgh">
            <img
              src="~/assets/images/nowruz.png"
              alt="Simurgh App"
              class="w-full h-56 object-cover object-top"
            />
          </NuxtLink>

          <div class="p-6">
            <h3 class="text-3xl font-bold mb-2 text-black">Nowruz</h3>
            <div class="flex"></div>
            <p class="text-gray-800">
              Celebrate Persian New Year and other Persian holidays with Nowruz.
              Get recipes, custom decorations, and event planning tools to make
              your celebration truly special.
            </p>
          </div>
          <div class="bg-gray-100 flex flex-row border-t-2 border-gray-200 p-6">
            <NuxtLink
              to="/apps/simurgh"
              class="text-blue-950 font-semibold py-2 px-6 rounded transition-all duration-500 hover:bg-yellow-400 bg-yellow-300"
            >
              Learn More
            </NuxtLink>
          </div>
        </div>
        <!-- end of app card -->
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: "Apps",
});
</script>

<style></style>
