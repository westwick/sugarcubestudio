<template>
  <PageHeader subtitle="Game Testing" title="Join the Simurgh Movement" />
  <div class="container py-16 mx-auto">
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mx-8">
      <div class="col-span-1 md:col-span-1">
        <img
          src="@/assets/images/simurghtest.jpg"
          alt="Simurgh Game Screenshot"
          class="w-full h-auto rounded-lg shadow-2xl"
        />
      </div>
      <div class="col-span-1 md:col-span-2 space-y-6">
        <div class="prose prose-lg text-white">
          <h2 class="mb-8 text-2xl font-bold">
            The voice of a nation has been silenced for too long.
          </h2>
          <p class="text-lg leading-relaxed mb-8">
            Imagine the courage it takes to stand up against a system built on
            tyranny and oppression. Simurgh is that courage, brought to life. It
            is an unyielding and passionate tribute to the people of Iran, a
            game born from the deep desire to see their beautiful country
            finally free.
          </p>
          <p class="text-lg leading-relaxed mb-8">
            This isn't just another mobile beat-'em-up. It's a statement. A
            declaration of war against the oppressive rulers who have held a
            nation captive. With stunning visuals and fluid, intense combat, you
            won't just be playing a game—you'll be part of a movement. Join the
            fight. Take control of Iran's destiny and become the hero a country
            so desperately needs. The battle for freedom starts now.
          </p>
          <div>
            <a
              href="https://forms.gle/BvWwjnx3xT6Njior8"
              target="_blank"
              rel="noopener noreferrer"
              class="inline-block bg-blue-500 text-white font-bold py-4 px-8 rounded transition-all duration-300"
            >
              Sign up to be a game tester!
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: "Game Tester - Simurgh",
  meta: [
    {
      name: "description",
      content:
        "Join the Simurgh movement as a game tester. Experience this powerful tribute to Iran's courage and fight for freedom in our mobile beat-'em-up game.",
    },
    { property: "og:title", content: "Game Tester - Simurgh" },
    {
      property: "og:description",
      content:
        "Join the Simurgh movement as a game tester. Experience this powerful tribute to Iran's courage and fight for freedom.",
    },
    {
      property: "og:url",
      content: "https://sugarcubestudio.netlify.app/game-tester",
    },
    { property: "og:type", content: "website" },
    { name: "twitter:card", content: "summary_large_image" },
    { name: "twitter:title", content: "Game Tester - Simurgh" },
    {
      name: "twitter:description",
      content:
        "Join the Simurgh movement as a game tester. Experience this powerful tribute to Iran's courage and fight for freedom.",
    },
  ],
});
</script>

<style scoped></style>
