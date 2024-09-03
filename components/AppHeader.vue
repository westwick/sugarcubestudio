<template>
  <header class="bg-gray-800">
    <div class="container mx-auto flex items-center py-4">
      <div class="flex space-x-4">
        <NuxtLink to="/" class="text-white text-lg md:text-xl font-bold" exact-active-class="text-yellow-400">
          Logo
        </NuxtLink>
        <NuxtLink to="/apps" class="text-white text-lg md:text-xl" exact-active-class="text-yellow-400">
          Apps
        </NuxtLink>
        <NuxtLink to="/contact" class="text-white text-lg md:text-xl" exact-active-class="text-yellow-400">
          Contact
        </NuxtLink>
      </div>
    </div>
  </header>
</template>
