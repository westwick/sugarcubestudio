<template>
  <div class="newsletter-bg bg-cover bg-center py-16">
    <div class="container mx-auto flex flex-col md:flex-row items-center my-20">
      <div class="md:w-1/2 mb-8 md:mb-0">
        <div
          class="max-w-md mx-auto bg-white p-8 rounded-lg shadow-lg border border-gray-200"
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
            />
            <button
              type="submit"
              class="w-full gradient-button text-white font-bold py-2 px-4 rounded"
            >
              Subscribe
            </button>
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
const email = ref("");

const submitForm = () => {
  console.log("Form submitted with email:", email.value);
};
</script>

<style scoped>
.newsletter-bg {
  background-image: url("@/assets/images/newsletter-bg.png");
}
</style>
