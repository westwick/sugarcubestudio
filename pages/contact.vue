<template>
  <div class="container mx-auto py-16 px-4 relative">
    <div class="absolute inset-0 z-0">
      <img
        src="@/assets/images/blur-transparent.png"
        alt="Background"
        class="w-full h-full object-cover"
      />
    </div>
    <div class="relative z-10">
      <h1 class="text-4xl font-bold mb-8 text-center text-white">
        Get in touch!
      </h1>
      <div
        class="max-w-2xl mx-auto bg-gray-900 bg-opacity-80 p-8 rounded-lg shadow-lg border border-gray-700"
      >
        <form
          @submit.prevent="handleSubmit"
          class="space-y-6"
          name="contact-page"
          netlify
        >
          <input type="hidden" name="form-name" value="contact-page" />
          <div>
            <label
              for="name"
              class="block text-sm font-medium text-gray-300 mb-1"
              >Name</label
            >
            <input
              type="text"
              id="name"
              name="name"
              v-model="name"
              required
              class="w-full px-4 py-2 rounded border border-gray-600 bg-gray-800 text-white focus:border-blue-500 focus:ring-1 focus:ring-blue-500 focus:outline-none"
            />
          </div>
          <div>
            <label
              for="email"
              class="block text-sm font-medium text-gray-300 mb-1"
              >Email</label
            >
            <input
              type="email"
              id="email"
              v-model="email"
              name="email"
              required
              class="w-full px-4 py-2 rounded border border-gray-600 bg-gray-800 text-white focus:border-blue-500 focus:ring-1 focus:ring-blue-500 focus:outline-none"
            />
          </div>
          <div>
            <label
              for="message"
              class="block text-sm font-medium text-gray-300 mb-1"
              >Message</label
            >
            <textarea
              id="message"
              v-model="message"
              rows="6"
              name="message"
              required
              class="w-full px-4 py-2 rounded border border-gray-600 bg-gray-800 text-white focus:border-blue-500 focus:ring-1 focus:ring-blue-500 focus:outline-none"
            ></textarea>
          </div>
          <div>
            <button
              type="submit"
              class="w-full gradient-button text-white font-bold py-2 px-4 rounded transition-all duration-300"
            >
              Send Message
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const name = ref("");
const email = ref("");
const message = ref("");

const handleSubmit = async () => {
  const formData = new URLSearchParams();
  formData.append("form-name", "contact-page");
  formData.append("name", name.value);
  formData.append("email", email.value);
  formData.append("message", message.value);

  try {
    const response = await fetch("/", {
      method: "POST",
      headers: { "Content-Type": "application/x-www-form-urlencoded" },
      body: formData.toString(),
    });

    if (response.ok) {
      // Clear form fields
      name.value = "";
      email.value = "";
      message.value = "";
      alert("Thank you for your message. We'll get back to you soon!");
    } else {
      throw new Error("Form submission failed");
    }
  } catch (error) {
    console.error("Error submitting form", error, JSON.stringify(error));
  }
};

useHead({
  title: "Contact",
  meta: [
    {
      name: "description",
      content: "Contact Sugar Cube Studio. We'd love to hear from you!",
    },
    { property: "og:title", content: "Contact Sugar Cube Studio" },
    {
      property: "og:description",
      content:
        "Get in touch with Sugar Cube Studio. We're here to answer your questions and hear your feedback.",
    },
    {
      property: "og:url",
      content: "https://sugarcubestudio.netlify.app/contact",
    },
    { property: "og:type", content: "website" },
  ],
});
</script>

<style scoped></style>
