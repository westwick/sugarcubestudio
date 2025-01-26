<template>
  <PageHeader
    subtitle="Our Applications"
    title="Explore our apps, all available on iOS and Android"
  />
  <div class="bg-gradient-to-t from-[rgb(215,223,232)] to-[rgb(244,246,248)]">
    <div class="container py-16 px-4 lg:px-0 mx-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mx-4">
        <div
          class="app-card bg-white rounded-lg overflow-hidden shadow-md flex flex-col h-full"
        >
          <NuxtLink to="/apps/simurgh">
            <img
              src="/bird.jpg"
              alt="Simurgh App"
              class="w-full h-64 object-cover"
            />
          </NuxtLink>

          <div class="p-6 flex-grow">
            <h3 class="text-3xl font-bold mb-2 text-black">Simurgh</h3>
            <div class="flex"></div>
            <p class="text-gray-800">
              Experience the epic adventure of Simurgh, where myth, history, and
              reality collide in a fight for freedom that will define the future
              of a nation.
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

        <div
          class="app-card bg-white rounded-lg overflow-hidden shadow-md flex flex-col h-full"
        >
          <NuxtLink to="/apps/nowruz">
            <img
              src="~/assets/images/nowruz.jpg"
              alt="Simurgh App"
              class="w-full h-64 object-cover object-top"
            />
          </NuxtLink>

          <div class="p-6 flex-grow">
            <h3 class="text-3xl font-bold mb-2 text-black">Nowruz</h3>
            <div class="flex"></div>
            <p class="text-gray-800">
              Celebrate the rich cultural heritage of Iran with the Nowruz app,
              your guide to the traditions, rituals, and festivities of the most
              important holidays Nowruz, Yalda Night, Cyrus day among others.
            </p>
          </div>
          <div class="bg-gray-100 flex flex-row border-t-2 border-gray-200 p-6">
            <NuxtLink
              to="/apps/nowruz"
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
