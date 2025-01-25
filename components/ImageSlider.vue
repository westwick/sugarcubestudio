<template>
  <div class="relative group">
    <div :class="containerClass" class="overflow-hidden">
      <div
        class="flex transition-transform duration-300 ease-in-out"
        :style="{ transform: `translateX(-${currentImageIndex * 100}%)` }"
      >
        <img
          v-for="(image, index) in images"
          :key="index"
          :src="image"
          :alt="`Image ${index + 1}`"
          class="shrink-0"
          :class="[
            aspectRatioClass,
            props.aspectRatio === '9/16' ? 'w-[80%] mx-[10%]' : 'w-full',
          ]"
        />
      </div>
      <!-- Navigation arrows -->
      <button
        @click="previousImage"
        class="absolute left-2 top-1/2 -translate-y-1/2 w-12 h-12 flex items-center justify-center bg-black bg-opacity-50 text-white rounded-full hover:bg-opacity-75 transition-all z-10"
      >
        <span class="sr-only">Previous</span>
        <ChevronLeft />
      </button>
      <button
        @click="nextImage"
        class="absolute right-2 top-1/2 -translate-y-1/2 w-12 h-12 flex items-center justify-center bg-black bg-opacity-50 text-white rounded-full hover:bg-opacity-75 transition-all z-10"
      >
        <span class="sr-only">Next</span>
        <ChevronRight />
      </button>
      <!-- Image indicators -->
      <div
        class="absolute bottom-4 left-1/2 transform -translate-x-1/2 flex space-x-2"
      >
        <button
          v-for="(_, index) in images"
          :key="index"
          @click="currentImageIndex = index"
          class="w-2 h-2 rounded-full"
          :class="index === currentImageIndex ? 'bg-white' : 'bg-white/50'"
        ></button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";
import { ChevronLeft, ChevronRight } from "lucide-vue-next";

const props = defineProps({
  images: {
    type: Array,
    required: true,
  },
  aspectRatio: {
    type: String,
    default: "16/9",
    validator: (value) => ["16/9", "9/16"].includes(value),
  },
});

const currentImageIndex = ref(0);

const nextImage = () => {
  currentImageIndex.value = (currentImageIndex.value + 1) % props.images.length;
};

const previousImage = () => {
  currentImageIndex.value =
    currentImageIndex.value === 0
      ? props.images.length - 1
      : currentImageIndex.value - 1;
};

const aspectRatioClass = computed(() => ({
  "aspect-[16/9]": props.aspectRatio === "16/9",
  "aspect-[9/16]": props.aspectRatio === "9/16",
}));

const containerClass = computed(() => ({
  "max-w-2xl mx-auto": props.aspectRatio === "16/9",
  "max-w-md mx-auto relative": props.aspectRatio === "9/16", // adjusted width for portrait
}));
</script>
