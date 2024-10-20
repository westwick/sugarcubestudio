<template>
  <PageHeader subtitle="Our Applications" title="Nowruz" />
  <div class="bg-white py-16">
    <div class="container mx-auto px-4">
      <div class="flex flex-col md:flex-row">
        <!-- Main content section (2/3 width on desktop) -->
        <div class="md:w-2/3 md:pr-8">
          <p class="mb-8 text-black text-lg">
            Nowruz, beautifully displays the most important dates in Persian
            culture. Always be connected to the Persian calendar with this
            interactive and convenient mobile app.
          </p>

          <!-- Screenshot section -->
          <div class="mb-8">
            <h2 class="text-2xl font-bold mb-4 text-black">Screenshots</h2>
            <div class="grid grid-cols-3 gap-2">
              <img
                src="~/assets/images/screenshot4.png"
                alt="Screenshot 1"
                class="w-full h-auto aspect-[9/16] object-cover rounded-lg shadow-md"
              />
              <img
                src="~/assets/images/screenshot1.png"
                alt="Screenshot 2"
                class="w-full h-auto aspect-[9/16] object-cover rounded-lg shadow-md"
              />
              <img
                src="~/assets/images/screenshot2.png"
                alt="Screenshot 3"
                class="w-full h-auto aspect-[9/16] object-cover rounded-lg shadow-md"
              />
            </div>
          </div>

          <!-- Additional information section -->
          <div class="text-black">
            <h2 class="text-2xl font-bold mb-4">Features</h2>
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
          <div class="bg-gray-100 p-6 rounded-lg">
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
useHead({
  meta: [
    { name: "description", content: "Test description for Nowruz." },
    { name: "og:site_name", content: "Sugar Cube Studio" },

    // Open Graph tags
    { property: "og:title", content: "Nowruz App by Sugar Cube Studio" },
    { property: "og:description", content: "SEO text for Nowruz" },
    {
      property: "og:url",
      content: "https://sugarcubestudio.netlify.app/apps/nowruz",
    },
    { property: "og:type", content: "website" },
    {
      property: "og:image",
      content: "https://sugarcubestudio.netlify.app/images/nowruz.png",
    },
    { property: "og:image:type", content: "image/png" },
    { property: "og:image:width", content: "256" },
    { property: "og:image:height", content: "256" },

    // Twitter Card tags
    { name: "twitter:card", content: "summary_large_image" },
    { name: "twitter:title", content: "My Custom Page Title" },
    {
      name: "twitter:description",
      content: "This is a custom page description for SEO and link previews.",
    },
    {
      name: "twitter:image",
      content: "https://sugarcubestudio.netlify.app/images/nowruz.png",
    },
  ],
});
</script>
