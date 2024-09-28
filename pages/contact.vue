<template>
  <div class="container mx-auto py-16 px-4">
    <h1 class="text-4xl font-bold mb-8 text-center text-white">
      Get in touch!
    </h1>
    <div
      class="max-w-2xl mx-auto bg-gray-900 p-8 rounded-lg shadow-lg border border-gray-700"
    >
      <form class="space-y-6" netlify>
        <div>
          <label for="name" class="block text-sm font-medium text-gray-300 mb-1"
            >Name</label
          >
          <input
            type="text"
            id="name"
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
</template>

<script setup lang="ts">
const name = ref("");
const email = ref("");
const message = ref("");

const submitForm = () => {
  console.log("Form submitted with data:", {
    name: name.value,
    email: email.value,
    message: message.value,
  });
  // Here you would typically send the form data to your backend or API
  // After successful submission, you might want to clear the form or show a success message
  name.value = "";
  email.value = "";
  message.value = "";
  alert("Thank you for your message. We'll get back to you soon!");
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
