<template>
  <PageHeader subtitle="Our Applications" title="Simurgh" />
  <div class="bg-white py-16">
    <div class="container mx-auto px-8">
      <div class="flex flex-col md:flex-row">
        <!-- Main content section (2/3 width on desktop) -->
        <div class="md:w-2/3 md:pr-8">
          <p class="mb-8 text-black text-xl">
            Simurgh, the mythical bird of Persian mythology, inspires this
            action packed experience. Step into the streets in this intense
            beat-em-up adventure. Play as a fearless woman challenging the
            status quo, fighting for her right to live freely.
          </p>

          <!-- Screenshot section -->
          <div class="mb-8 relative">
            <h2 class="text-md font-bold text-gray-500 uppercase">
              Screenshots
            </h2>
            <ImageSlider :images="screenshots" aspect-ratio="16/9" />
          </div>
          <!-- Music section -->
          <div class="mb-8">
            <h2 class="text-md font-bold mb-4 text-gray-500 uppercase">
              Featuring Original Music
            </h2>
            <p class="text-black">
              Simurgh features an original soundtrack using traditional Persian
              instruments such as the Ney, Santur, and Tombak to craft a unique
              and immersive musical experience to keep you engaged. Full
              soundtrack available on
              <a
                href="https://www.youtube.com/@sugarcubestudio"
                target="_blank"
                class="text-blue-500"
                >Youtube</a
              >
              and Spotify.
            </p>
          </div>

          <!-- Additional information section -->
          <div class="text-black">
            <h2 class="text-md font-bold mb-4 text-gray-500 uppercase">
              More Features
            </h2>
            <ul class="list-disc list-inside">
              <li>Intense beat-em-up gameplay</li>
              <li>Stunning Persian-inspired visuals</li>
              <li>Compelling storyline</li>
              <li>Multiple challenging levels</li>
            </ul>
          </div>
        </div>

        <!-- Downloads section (1/3 width on desktop) -->
        <div class="md:w-1/3 mb-8 md:mb-0">
          <div class="bg-gray-100 p-6 rounded-lg sticky top-4 mt-8 md:mt-0">
            <h2 class="text-2xl font-bold mb-4 text-black">Download Links</h2>
            <p class="text-gray-500 mb-4">Coming Soon!</p>
            <!-- <div class="flex space-x-4">
              <a href="#" class="">
                <img
                  src="~/assets/images/ios-badge.png"
                  alt="Download on App Store"
                  class="w-48 h-auto mb-4"
                />
              </a>
              <a href="#" class="">
                <img
                  src="~/assets/images/play-badge.png"
                  alt="Download onGoogle Play"
                  class="w-48 h-auto"
                />
              </a>
            </div> -->
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import screenshot1 from "~/assets/simurgh/2024-10-16-07h54m38s347.jpg";
import screenshot2 from "~/assets/simurgh/2024-10-16-08h31m41s931.jpg";
import screenshot3 from "~/assets/simurgh/Screenshot_20241014-210110.jpg";

const screenshots = [screenshot1, screenshot2, screenshot3];
</script>
