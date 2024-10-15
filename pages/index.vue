<template>
  <AppHero />
  <div class="bg-white">
    <section class="angled-section py-4 md:py-8">
      <div class="container mx-auto text-center">
        <p
          class="text-lg md:text-xl max-w-64 md:max-w-lg px-8 mx-auto text-slate-400 italic"
        >
          Innovations driven by imagination.
        </p>
      </div>
    </section>
    <section>
      <HomeNewsletter />
    </section>
    <section
      class="bg-gradient-to-t from-[rgb(215,223,232)] to-[rgb(244,246,248)]"
    >
      <HomeApps />
    </section>
    <section>
      <HomeNews />
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  meta: [
    {
      name: "description",
      content: "This is a custom page description for SEO and link previews.",
    },

    // Open Graph tags
    { property: "og:title", content: "Sugar Cube Studio" },
    {
      property: "og:description",
      content: "This is a custom page description for SEO and link previews.",
    },
    { property: "og:image", content: "https://example.com/og-image.jpg" }, // Replace with your image URL
    { property: "og:url", content: "https://sugarcubestudio.netlify.app/" },
    { property: "og:type", content: "website" },

    // Twitter Card tags
    { name: "twitter:card", content: "summary_large_image" },
    { name: "twitter:title", content: "My Custom Page Title" },
    {
      name: "twitter:description",
      content: "This is a custom page description for SEO and link previews.",
    },
    { name: "twitter:image", content: "https://example.com/twitter-image.jpg" }, // Replace with your image URL
  ],
});
</script>

<style>
.angled-section {
  background: #1e1f33;
  position: relative;
  clip-path: polygon(
    -20px 0px,
    calc(100% + 20px) 0px,
    calc(100% - 100px) 100%,
    100px 100%
  );
}
</style>
