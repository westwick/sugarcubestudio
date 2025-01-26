<template>
  <div class="page-header py-16 text-left">
    <div class="container mx-auto px-8">
      <p class="text-gray-400 text-lg mb-4 uppercase">{{ subtitle }}</p>
      <h1 class="text-2xl md:text-4xl font-bold text-white">{{ title }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    subtitle: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
  },
};
</script>

<style>
.page-header {
  background: url("~/assets/images/page-header-bg.jpg") no-repeat center;
  background-size: cover;
}
</style>
