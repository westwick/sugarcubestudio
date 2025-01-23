<template>
  <PageHeader subtitle="Our Applications" title="Nowruz" />
  <div class="bg-white py-16">
    <div class="container mx-auto px-4">
      <div class="flex flex-col md:flex-row">
        <!-- Main content section (2/3 width on desktop) -->
        <div class="md:w-2/3 md:pr-8">
          <p class="mb-8 text-black text-lg">
            Celebrate Persian culture and traditions with this beautifully
            crafted app, designed to bring the essence of Nowruz and other
            beloved festivities to life. Explore engaging features that
            highlight events like Yalda Night, Cyrus Day, Sizdah Bedar and
            Chaharshanbeh Soori, offering insights and interactive elements for
            all ages. Whether you're reconnecting with your roots or discovering
            something new, this app is your guide to timeless celebrations.
          </p>

          <!-- Screenshot section -->
          <div class="mb-8">
            <h2 class="text-2xl font-bold mb-4 text-black">Screenshots</h2>
            <ImageSlider :images="screenshots" aspect-ratio="9/16" />
          </div>

          <!-- Additional information section -->
          <div class="text-black">
            <h2 class="text-2xl font-bold mb-4">Features</h2>
            <ul class="list-disc list-inside">
              <li>Celebrate Persian traditions</li>
              <li>Interactive festive activities</li>
              <li>Cultural insights and history</li>
              <li>Vibrant holiday reminders</li>
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
import screenshot1 from "~/assets/images/screenshot4.png";
import screenshot2 from "~/assets/images/screenshot1.png";
import screenshot3 from "~/assets/images/screenshot2.png";

const screenshots = [screenshot1, screenshot2, screenshot3];

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
