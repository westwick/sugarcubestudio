<template>
  <PageHeader subtitle="Our Applications" title="Simurgh" />
  <div class="bg-white py-16">
    <div class="container mx-auto px-4">
      <div class="flex flex-col md:flex-row">
        <!-- Main content section (2/3 width on desktop) -->
        <div class="md:w-2/3 md:pr-8">
          <p class="mb-8 text-black text-xl">
            Simurgh, the mythical bird of Persian mythology, inspires this
            action packed experience. Step into the streets in this intense
            beat-em-up adventure. Play as a fearless woman challenging the
            status quo, fighting for her right to live freely.
          </p>

          <!-- Music section -->
          <div class="mb-8">
            <h2 class="text-md font-bold mb-4 text-gray-500 uppercase">
              Featuring Original Music
            </h2>
            <p class="text-black">
              Simurgh features an original soundtrack using traditional Persian
              instruments such as the Ney, Santur, and Tombak to craft a unique
              and immersive musical experience to keep you engaged.
              <a href="#" class="text-blue-500">Click here</a> to listen to the
              full soundtrack on youtube.
            </p>
          </div>

          <!-- Screenshot section -->
          <div class="mb-8 relative">
            <h2 class="text-md font-bold mb-4 text-gray-500 uppercase">
              Screenshots
            </h2>
            <div class="relative group">
              <img
                :src="screenshots[currentImageIndex]"
                :alt="`Screenshot ${currentImageIndex + 1}`"
                class="w-full h-auto aspect-auto object-cover rounded-lg shadow-md"
              />
              <!-- Navigation arrows -->
              <button
                @click="previousImage"
                class="absolute left-0 top-1/2 -translate-x-6 -translate-y-1/2 w-12 h-12 flex items-center justify-center bg-black bg-opacity-50 text-white rounded-full hover:bg-opacity-75 transition-all"
              >
                <span class="sr-only">Previous</span>
                &#8592;
                <!-- Left arrow -->
              </button>
              <button
                @click="nextImage"
                class="absolute right-0 top-1/2 translate-x-6 -translate-y-1/2 w-12 h-12 flex items-center justify-center bg-black bg-opacity-50 text-white rounded-full hover:bg-opacity-75 transition-all"
              >
                <span class="sr-only">Next</span>
                &#8594;
                <!-- Right arrow -->
              </button>
              <!-- Image indicators -->
              <div
                class="absolute bottom-4 left-1/2 transform -translate-x-1/2 flex space-x-2"
              >
                <button
                  v-for="(_, index) in screenshots"
                  :key="index"
                  @click="currentImageIndex = index"
                  class="w-2 h-2 rounded-full"
                  :class="
                    index === currentImageIndex ? 'bg-white' : 'bg-white/50'
                  "
                ></button>
              </div>
            </div>
          </div>

          <!-- Additional information section -->
          <div class="text-black">
            <h2 class="text-md font-bold mb-4 text-gray-500 uppercase">
              Features
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
          <div class="bg-gray-100 p-6 rounded-lg sticky top-4">
            <h2 class="text-2xl font-bold mb-4 text-black">Download Links</h2>
            <p class="text-gray-500 mb-4">Available on iOS and Android:</p>
            <div class="flex space-x-4">
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
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

// Import images directly
import screenshot1 from "~/assets/simurgh/2024-10-16-07h54m38s347.png";
import screenshot2 from "~/assets/simurgh/2024-10-16-08h31m41s931.png";
import screenshot3 from "~/assets/simurgh/Screenshot_20241014-210110.png";

const screenshots = [screenshot1, screenshot2, screenshot3];

const currentImageIndex = ref(0);

const nextImage = () => {
  currentImageIndex.value = (currentImageIndex.value + 1) % screenshots.length;
};

const previousImage = () => {
  currentImageIndex.value =
    currentImageIndex.value === 0
      ? screenshots.length - 1
      : currentImageIndex.value - 1;
};
</script>
