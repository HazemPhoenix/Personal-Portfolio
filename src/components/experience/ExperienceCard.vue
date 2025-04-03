<template>
  <div
    class="h-[20vh] flex items-center gap-4 overflow-hidden bg-gray-200 dark:bg-linear-to-r dark:from-[#04071D] dark:to-[#0C0E23] px-6 py-4 rounded-2xl border border-gray-400 dark:border-[#1e2230] shadow-lg"
  >
    <div class="w-25 h-20 flex-shrink-0">
      <img :src="src" class="w-full h-full object-contain" />
    </div>
    <div class="flex flex-col">
      <h2
        class="text-gray-800 dark:text-white text-md md:text-lg font-semibold"
      >
        {{ title }}
      </h2>
      <p class="text-gray-600 dark:text-gray-400 text-xs md:text-sm">
        {{ description }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    src: {
      type: String,
      required: true,
    },
  },
};
</script>
