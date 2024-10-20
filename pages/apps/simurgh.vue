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
              Simurgh features an original soundtrack composed by
              <em>composer name</em>, who uses traditional Persian instruments
              such as the Ney, Santur, and Tombak to craft a unique and
              immersive musical experience to keep you engaged.
              <a href="#" class="text-blue-500">Click here</a> to listen to the
              full soundtrack on youtube.
            </p>
          </div>

          <!-- Screenshot section -->
          <div class="mb-8">
            <h2 class="text-md font-bold mb-4 text-gray-500 uppercase">
              Screenshots
            </h2>
            <div class="grid grid-rows-3 gap-2">
              <img
                src="~/assets/simurgh/2024-10-16-07h54m38s347.png"
                alt="Screenshot 1"
                class="w-full h-auto aspect-auto object-cover rounded-lg shadow-md"
              />
              <img
                src="~/assets/simurgh/2024-10-16-08h31m41s931.png"
                alt="Screenshot 2"
                class="w-full h-auto aspect-auto object-cover rounded-lg shadow-md"
              />
              <img
                src="~/assets/simurgh/Screenshot_20241014-210110.png"
                alt="Screenshot 3"
                class="w-full h-auto aspect-auto object-cover rounded-lg shadow-md"
              />
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
