<template>
  <div class="newsletter-bg bg-cover bg-center py-16">
    <div class="container mx-auto flex flex-col md:flex-row items-center my-20">
      <div class="md:w-1/2 mb-8 md:mb-0">
        <div
          class="max-w-md bg-white p-8 rounded-lg shadow-lg border border-gray-200 m-4"
        >
          <h2 class="text-black font-bold text-xl mb-4">
            Be the first to know when we launch new stuff.
          </h2>
          <form @submit.prevent="submitForm">
            <input
              type="email"
              v-model="email"
              placeholder="Enter your email"
              class="text-black w-full px-4 py-2 mb-4 rounded border border-gray-300 focus:border-blue-500 focus:ring-1 focus:outline-none"
              required
              :disabled="loading"
            />
            <button
              type="submit"
              class="w-full gradient-button text-white font-bold py-2 px-4 rounded"
              :disabled="loading"
            >
              {{ loading ? "Subscribing..." : "Subscribe" }}
            </button>
            <p
              v-if="message"
              class="mt-4 text-center text-black"
              :class="{ 'text-green-600': !message.includes('Sorry') }"
            >
              {{ message }}
            </p>
          </form>
        </div>
      </div>
      <div class="md:w-1/2">
        <p class="max-w-xl mx-auto"></p>
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
</script>

<style scoped>
.newsletter-bg {
  background-image: url("/public/images/Tomb.png");
}
</style>
