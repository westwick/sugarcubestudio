<template>
  <h1>Home</h1>
  <p>Sugar Cube Studio</p>
</template>

<script setup lang="ts">
useHead({
  meta: [
    { name: 'description', content: 'This is a custom page description for SEO and link previews.' },

    // Open Graph tags
    { property: 'og:title', content: 'Sugar Cube Studio' },
    { property: 'og:description', content: 'This is a custom page description for SEO and link previews.' },
    { property: 'og:image', content: 'https://example.com/og-image.jpg' }, // Replace with your image URL
    { property: 'og:url', content: 'https://sugarcubestudio.netlify.app/' },
    { property: 'og:type', content: 'website' },

    // Twitter Card tags
    { name: 'twitter:card', content: 'summary_large_image' },
    { name: 'twitter:title', content: 'My Custom Page Title' },
    { name: 'twitter:description', content: 'This is a custom page description for SEO and link previews.' },
    { name: 'twitter:image', content: 'https://example.com/twitter-image.jpg' }, // Replace with your image URL
  ],
})
</script>
