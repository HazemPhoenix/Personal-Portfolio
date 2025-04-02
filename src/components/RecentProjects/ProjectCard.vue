<template>
  <div
    class="border-1 border-gray-400 dark:border-[#3637496E] rounded-xl flex flex-col gap-5 py-5 px-4 bg-linear-to-r from-gray-100 to-gray-200 dark:from-[#04071D] dark:to-[#0C0E23]"
  >
    <div class="rounded-xl overflow-hidden">
      <img src="@/assets/images/projects/reservio.png" :alt="alt" />
    </div>
    <h2 class="text-[24px] md:size-[32px] text-gray-800 dark:text-white">
      {{ title }}
    </h2>
    <p class="text-[14px] text-gray-700 dark:text-[#BEC1DD]">
      {{ description }}
    </p>
    <div class="flex justify-between">
      <div class="flex">
        <div class="border-1 border-[#3637496E] rounded-full p-1">
          <img
            src="@/assets/svg/vue.svg"
            alt="Technology"
            class="w-6 h-6 inline-block"
          />
        </div>

        <div class="border-1 border-[#3637496E] rounded-full p-1">
          <img
            src="@/assets/svg/tailwind.svg"
            alt="Technology"
            class="w-6 h-6 inline-block"
          />
        </div>

        <div class="border-1 border-[#3637496E] rounded-full p-1">
          <img
            src="@/assets/svg/firebase.svg"
            alt="Technology"
            class="w-6 h-6 inline-block"
          />
        </div>

        <div class="border-1 border-[#3637496E] rounded-full p-1">
          <img
            src="@/assets/svg/express.svg"
            alt="Technology"
            class="w-6 h-6 inline-block"
          />
        </div>
      </div>
      <a
        :href="link"
        target="_blank"
        class="flex items-center gap-1 dark:text-gray-300 hover:dark:text-white hover:text-black"
        >Check Live Site
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          fill="currentColor"
          class="size-4 rotate-180"
        >
          <path
            fill-rule="evenodd"
            d="M20.03 3.97a.75.75 0 0 1 0 1.06L6.31 18.75h9.44a.75.75 0 0 1 0 1.5H4.5a.75.75 0 0 1-.75-.75V8.25a.75.75 0 0 1 1.5 0v9.44L18.97 3.97a.75.75 0 0 1 1.06 0Z"
            clip-rule="evenodd"
          />
        </svg>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: ["src", "alt", "title", "description", "link", "technologies"],
};
</script>
