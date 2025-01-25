<template>
  <div class="py-16 relative overflow-hidden">
    <div class="container mx-auto">
      <div class="flex flex-col md:flex-row items-center">
        <div
          class="w-full md:w-1/2 md:order-1 order-2 relative h-64 md:h-96 mt-8 md:mt-0"
        >
          <img
            :src="appMockupImage"
            alt="App Mockup"
            class="absolute w-full max-w-md mx-auto px-4 left-0 right-0 object-contain app-mockup"
          />
        </div>
        <div
          class="w-full px-8 pb-32 md:pb-0 md:px-0 md:w-1/2 md:pl-8 order-1 md:order-2"
        >
          <h2 class="text-3xl font-bold mb-6 text-black">Our Apps</h2>
          <p class="text-lg mb-6 text-gray-800">
            Discover immersive experiences that bring culture, history, and
            adventure to life, offering unique journeys through powerful stories
            and meaningful traditions. Whether you're exploring new worlds or
            celebrating timeless rituals, these apps are designed to engage,
            inspire, and connect you with something truly extraordinary.
          </p>
          <NuxtLink
            to="/apps"
            class="gradient-button text-white font-bold py-2 px-4 rounded inline-block"
          >
            Explore Our Apps
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import appMockupImage from "~/assets/images/nowruz-mockup.png";
// made with mockuphone.com
</script>

<style scoped>
.app-mockup {
  bottom: -150px; /* Mobile view: Adjust this value as needed */
}

@media (min-width: 768px) {
  .app-mockup {
    bottom: -140px; /* Medium and up: Adjust this value for desktop as needed */
  }
}
</style>
