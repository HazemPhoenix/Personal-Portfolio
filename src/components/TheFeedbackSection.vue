<template>
  <section
    id="testimonials"
    class="py-12 px-6 dark:text-white text-center flex flex-col gap-10 mt-10"
  >
    <h2 class="text-center text-2xl md:text-5xl font-bold">
      Kind words from
      <span class="text-[#7519ff] dark:text-[#CBACF9]">satisfied clients</span>
    </h2>
    <div class="relative max-w-4xl mx-auto">
      <div
        class="overflow-hidden relative rounded-lg bg-gray-200 dark:bg-linear-to-r dark:from-[#04071D] dark:to-[#0C0E23] p-6 min-h-[200px] backdrop-blur-lg"
      >
        <div class="absolute inset-0 overflow-hidden">
          <div
            class="absolute w-[150px] h-[150px] rounded-full dark:bg-sky-300/15 bg-[#7519ff]/30 animate-pulse blur-[60px] -top-8 left-[20%]"
          ></div>
          <div
            class="absolute w-[200px] h-[200px] rounded-full dark:bg-sky-300/15 bg-[#7519ff]/30 animate-pulse blur-[60px] -bottom-12 right-[20%]"
          ></div>
        </div>
        <transition name="fade" mode="out-in">
          <ReviewCard
            :key="currentTestimonial.id"
            :currentTestimonial="currentTestimonial"
          />
        </transition>
      </div>
      <div class="flex justify-center mt-4 gap-2">
        <span
          v-for="(t, index) in testimonials"
          :key="t.id"
          @click="currentIndex = index"
          class="w-3 h-3 rounded-full cursor-pointer"
          :class="index === currentIndex ? 'bg-purple-400' : 'bg-gray-600'"
        >
        </span>
      </div>
    </div>
  </section>
</template>

<script>
import ReviewCard from "./testimonials/ReviewCard.vue";

export default {
  data() {
    return {
      testimonials: [
        {
          id: 1,
          text: "Collaborating with Hazem was an absolute pleasure. His professionalism, promptness, and dedication to delivering exceptional results were evident throughout our project.",
          name: "Michael Johnson",
          position: "Director of AlphaStream Technologies",
        },
        {
          id: 2,
          text: "Collaborating with Hazem was an absolute pleasure. His professionalism, promptness, and dedication to delivering exceptional results were evident throughout our project.",
          name: "Michael Johnson",
          position: "Director of AlphaStream Technologies",
        },
        {
          id: 3,
          text: "Collaborating with Hazem was an absolute pleasure. His professionalism, promptness, and dedication to delivering exceptional results were evident throughout our project.",
          name: "Michael Johnson",
          position: "Director of AlphaStream Technologies",
        },
      ],
      currentIndex: 0,
    };
  },
  components: {
    ReviewCard,
  },
  computed: {
    currentTestimonial() {
      return this.testimonials[this.currentIndex];
    },
  },
  mounted() {
    setInterval(() => {
      this.currentIndex = (this.currentIndex + 1) % this.testimonials.length;
    }, 5000);
  },
};
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
