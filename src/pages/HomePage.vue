<template>
  <!-- Parent container to hold the grid/spotlight overlay -->
  <div
    class="relative w-full min-h-screen bg-[#000319] text-white overflow-hidden absolute z-50"
  >
    <!-- The pseudo-element (for the grid + spotlights) is added in <style> below -->

    <TheNavbar current="about" />
    <TheHeader />
    <TheMainSection />
    <TheRecentProjectsSection />
    <TheExperienceSection />
    <TheApproachSection />
    <TheFeedbackSection />
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
      transparent 80px
    ),
    repeating-linear-gradient(
      to right,
      rgba(255, 255, 255, 0.04) 0,
      rgba(255, 255, 255, 0.04) 1px,
      transparent 1px,
      transparent 80px
    );
}
</style>
