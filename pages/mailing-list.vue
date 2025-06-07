<template>
  <PageHeader subtitle="Join Our Mailing List" title="Stay Updated" />
  <div
    class="container mx-auto px-4 relative min-h-[600px] flex items-center justify-center"
  >
    <div class="absolute inset-0 z-0">
      <img
        src="@/assets/images/blur-transparent.png"
        alt="Background"
        class="w-full h-full object-cover"
      />
    </div>
    <div class="relative z-10 w-full flex items-center justify-center">
      <div
        class="signup-form max-w-2xl w-full bg-gray-900 bg-opacity-80 rounded-lg shadow-2xl border border-gray-700 flex flex-col items-center"
      >
        <p class="text-gray-300 mb-6 text-center text-lg">
          Be the first to know about our latest updates and releases.
        </p>
        <form @submit.prevent="submitForm" class="space-y-6 w-full max-w-md">
          <div>
            <label
              for="email"
              class="block text-sm font-medium text-gray-300 mb-1"
              >Email</label
            >
            <input
              type="email"
              id="email"
              placeholder="Enter your email"
              v-model="email"
              required
              class="w-full px-4 py-2 rounded border border-gray-600 bg-gray-800 text-white focus:border-blue-500 focus:ring-1 focus:ring-blue-500 focus:outline-none"
              :disabled="loading"
            />
          </div>
          <div>
            <button
              type="submit"
              class="w-full gradient-button text-white font-bold py-2 px-4 rounded transition-all duration-300"
              :disabled="loading"
            >
              {{ loading ? "Subscribing..." : "Subscribe" }}
            </button>
          </div>
          <p
            v-if="message"
            class="text-center"
            :class="{
              'text-green-400': !message.includes('Sorry'),
              'text-red-400': message.includes('Sorry'),
            }"
          >
            {{ message }}
          </p>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const email = ref("");
const loading = ref(false);
const message = ref("");

const submitForm = async () => {
  loading.value = true;
  message.value = "";

  try {
    const response = await fetch(
      "https://connect.mailerlite.com/api/subscribers",
      {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
          Accept: "application/json",
          Authorization: `Bearer ${import.meta.env.VITE_MAILERLITE_API_KEY}`,
        },
        body: JSON.stringify({
          email: email.value,
        }),
      }
    );

    if (!response.ok) {
      throw new Error("Subscription failed");
    }

    message.value = "Thank you for subscribing!";
    email.value = "";
  } catch (error) {
    console.error("Error:", error);
    message.value = "Sorry, something went wrong. Please try again later.";
  } finally {
    loading.value = false;
  }
};

useHead({
  title: "Join Our Mailing List",
  meta: [
    {
      name: "description",
      content:
        "Subscribe to Sugar Cube Studio's mailing list to stay updated with our latest news and releases.",
    },
    {
      property: "og:title",
      content: "Join Our Mailing List - Sugar Cube Studio",
    },
    {
      property: "og:description",
      content:
        "Subscribe to our mailing list and be the first to know about our latest updates and releases.",
    },
    {
      property: "og:url",
      content: "https://sugarcubestudio.netlify.app/mailing-list",
    },
    { property: "og:type", content: "website" },
  ],
});
</script>

<style scoped>
.signup-form {
  padding: 80px;
}
</style>
