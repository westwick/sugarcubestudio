<template>
  <Teleport to="body">
    <div v-if="isOpen" class="fixed inset-0 z-50 overflow-y-auto">
      <!-- Backdrop -->
      <div
        class="fixed inset-0 bg-black bg-opacity-50 transition-opacity"
        @click="close"
      ></div>

      <!-- Modal -->
      <div class="flex min-h-full items-center justify-center p-4">
        <div class="relative bg-white rounded-lg w-full max-w-md p-6">
          <!-- Close button -->
          <button
            @click="close"
            class="absolute top-4 right-4 text-gray-400 hover:text-gray-500"
          >
            <span class="sr-only">Close</span>
            <svg
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>

          <!-- Content -->
          <div class="text-center">
            <h3 class="text-xl font-semibold text-gray-900 mb-2">
              Join our mailing list!
            </h3>
            <p class="text-gray-600 mb-4">
              Be the first to know when we launch new stuff.
            </p>

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
                class="w-full gradient-button font-semibold py-2 px-4 rounded"
                :disabled="loading"
              >
                {{ loading ? "Subscribing..." : "Subscribe" }}
              </button>
              <p
                v-if="message"
                class="mt-4 text-center text-black"
                :class="{
                  'text-green-600': !message.includes('Sorry'),
                  'text-red-600': message.includes('Sorry'),
                }"
              >
                {{ message }}
              </p>
            </form>
          </div>
        </div>
      </div>
    </div>
  </Teleport>
</template>

<script setup>
import { ref } from "vue";

const isOpen = ref(false);
const email = ref("");
const loading = ref(false);
const message = ref("");

const open = () => {
  isOpen.value = true;
  message.value = "";
  email.value = "";
};

const close = () => {
  isOpen.value = false;
};

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

defineExpose({ open });
</script>
