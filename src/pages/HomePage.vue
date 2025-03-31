<template>
  <div
    class="dark:bg-[#000319] bg-gray-100 dark:text-white text-gray-800 w-full min-h-screen flex flex-col px-2 md:px-0"
  >
    <ToggleDarkMode />
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
