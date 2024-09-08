<template>
    <section class="bg-white text-black min-h-96">
        <h1>Nowruz</h1>
    </section>
</template>

<script setup>
useHead({
  meta: [
    { name: 'description', content: 'Test description for Nowruz.' },

    // Open Graph tags
    { property: 'og:title', content: 'Nowruz App by Sugar Cube Studio' },
    { property: 'og:description', content: 'SEO text for Nowruz' },
    { property: 'og:image', content: 'https://sugarcubestudio.netlify.app/images/nowruz.png' },
    { property: 'og:url', content: 'https://sugarcubestudio.netlify.app/apps/nowruz' },
    { property: 'og:type', content: 'website' },

    // Twitter Card tags
    { name: 'twitter:card', content: 'summary_large_image' },
    { name: 'twitter:title', content: 'My Custom Page Title' },
    { name: 'twitter:description', content: 'This is a custom page description for SEO and link previews.' },
    { name: 'twitter:image', content: 'https://example.com/twitter-image.jpg' }, // Replace with your image URL
  ],
})
</script>