<template>
  <div class="p-4 relative">
    <p class="text-md md:text-lg text-gray-900 dark:text-gray-200">
      {{ currentTestimonial.text }}
    </p>
    <div class="flex items-center mt-4 space-x-3 justify-center">
      <img
        src="@/assets/images/reviewer.png"
        alt="Client"
        class="w-10 h-10 rounded-full"
      />
      <div>
        <p class="font-semibold">{{ currentTestimonial.name }}</p>
        <p class="text-sm text-gray-600 dark:text-gray-400">
          {{ currentTestimonial.position }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    currentTestimonial: {
      type: Object,
      required: true,
    },
  },
};
</script>
