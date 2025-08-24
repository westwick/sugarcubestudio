<template>
  <div class="py-16 px-8 container mx-auto text-center">
    <h2 class="text-black font-bold text-2xl mb-8">Latest News and Updates</h2>

    <div class="news-grid">
      <!-- News Card 1 -->
      <div class="news-card">
        <div class="news-image-placeholder"></div>
        <div class="news-content">
          <h3 class="news-headline">Teaser Release</h3>
          <p class="news-text">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </p>
        </div>
      </div>

      <!-- News Card 2 -->
      <div class="news-card">
        <div class="news-image-placeholder"></div>
        <div class="news-content">
          <h3 class="news-headline">News Headline 2</h3>
          <p class="news-text">
            Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
            nisi ut aliquip ex ea commodo consequat.
          </p>
        </div>
      </div>

      <!-- News Card 3 -->
      <div class="news-card">
        <div class="news-image-placeholder"></div>
        <div class="news-content">
          <h3 class="news-headline">News Headline 3</h3>
          <p class="news-text">
            Duis aute irure dolor in reprehenderit in voluptate velit esse
            cillum dolore eu fugiat nulla pariatur.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// Component logic (if any) goes here
</script>

<style scoped>
.news-grid {
  @apply grid grid-cols-1 md:grid-cols-3 gap-8 mx-4 md:mx-0 text-left;
}

.news-card {
  @apply bg-white rounded-lg shadow-md overflow-hidden;
}

.news-image-placeholder {
  @apply w-full h-48 bg-gradient-to-r from-blue-400 to-purple-500;
}

.news-content {
  @apply p-6;
}

.news-headline {
  @apply font-bold text-xl mb-2 text-gray-900;
}

.news-text {
  @apply text-gray-700;
}
</style>
