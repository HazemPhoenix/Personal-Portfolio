<template>
  <div
    class="relative w-full min-h-screen bg-gray-100 text-gray-800 dark:bg-[#000319] dark:text-white overflow-hidden z-50 px-5 md:px-20"
  >
    <ToggleDarkMode />
    <TheNavbar />
    <TheHeader />
    <TheMainSection />
    <TheRecentProjectsSection />
    <TheFeedbackSection />
    <TheExperienceSection />
    <TheApproachSection />
    <TheFooter />
  </div>
</template>

<script>
import TheApproachSection from "@/components/TheApproachSection.vue";
import TheExperienceSection from "@/components/TheExperienceSection.vue";
import TheFeedbackSection from "@/components/TheFeedbackSection.vue";
import TheFooter from "@/components/TheFooter.vue";
import TheHeader from "@/components/TheHeader.vue";
import TheMainSection from "@/components/TheMainSection.vue";
import TheNavbar from "@/components/TheNavbar.vue";
import TheRecentProjectsSection from "@/components/TheRecentProjectsSection.vue";
import ToggleDarkMode from "@/components/ToggleDarkMode.vue";

export default {
  components: {
    TheNavbar,
    TheHeader,
    TheMainSection,
    TheRecentProjectsSection,
    TheFeedbackSection,
    TheExperienceSection,
    TheApproachSection,
    TheFooter,
    ToggleDarkMode,
  },
};
</script>

<style scoped>
.relative::before {
  content: "";
  position: absolute;
  inset: 0;
  z-index: -1;
  pointer-events: none;

  background: repeating-linear-gradient(
      to bottom,
      rgba(255, 255, 255, 0.04) 0,
      rgba(255, 255, 255, 0.04) 1px,
      transparent 1px,
      transparent 90px
    ),
    repeating-linear-gradient(
      to right,
      rgba(255, 255, 255, 0.04) 0,
      rgba(255, 255, 255, 0.04) 1px,
      transparent 1px,
      transparent 90px
    );
}
</style>
