<template>
  <div class="bg-[#000319] text-white h-[100vh] pt-10">
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
