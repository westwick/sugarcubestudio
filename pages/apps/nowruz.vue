<template>
  <PageHeader subtitle="Our Applications" title="Nowruz" />
  <div
    class="relative w-full h-96 items-center justify-center bg-cover bg-center"
    :style="{ backgroundImage: 'url(/images/nowruz.png)' }"
  >
    <h1>Nowruz</h1>
  </div>
  <div class="container mx-auto">
    <p class="my-10 md:text-2xl text-lg">
      Nowruz, beautifully displays the most important dates in Persian culture.
      <br />Always be connected to the Persian calendar with this interactive
      and convenient mobile app.
    </p>
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
