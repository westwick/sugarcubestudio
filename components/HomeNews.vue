<template>
  <div class="py-16 px-8 container mx-auto text-center">
    <h2 class="text-black font-bold text-2xl mb-8">Latest News and Updates</h2>

    <div class="news-grid">
      <!-- News Card 1 -->
      <div class="news-card">
        <div class="news-image-placeholder"></div>
        <div class="news-content">
          <h3 class="news-headline">Simurgh Teaser Released on Instagram</h3>
          <p class="news-text">
            Teaser for the Simurgh mobile game has been released for Instagram.
          </p>
          <p>
            <a
              href="https://www.instagram.com/p/DNtXrAhWnPR/"
              target="_blank"
              rel="noopener noreferrer"
              class="text-blue-600 underline"
            >
              View on Instagram
            </a>
          </p>
        </div>
      </div>

      <!-- News Card 2 -->
      <div class="news-card">
        <div class="news-image-placeholder"></div>
        <div class="news-content">
          <h3 class="news-headline">Simurgh Teaser Released on YouTube</h3>
          <p class="news-text">
            Teaser for the Simurgh mobile game has been released for YouTube.
          </p>
          <p>
            <a
              href="https://www.youtube.com/shorts/dyVXUoq0_VE"
              target="_blank"
              rel="noopener noreferrer"
              class="text-blue-600 underline"
            >
              View on Instagram
            </a>
          </p>
        </div>
      </div>

      <!-- News Card 3 -->
      <div class="news-card">
        <div class="news-image-placeholder"></div>
        <div class="news-content">
          <h3 class="news-headline">Simurgh Game Testers</h3>
          <p class="news-text">
            We are looking for game testers for our game Simurgh.
          </p>
          <p>
            <a
              href="https://sugarcubestudio.com/game-tester"
              target="_blank"
              rel="noopener noreferrer"
              class="text-blue-600 underline"
            >
              Sign Up Today!!
            </a>
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
