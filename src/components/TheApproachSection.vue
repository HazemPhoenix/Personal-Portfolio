<template>
  <section class="mt-10 md:mt-20">
    <h2 class="text-center text-2xl md:text-5xl font-bold">
      My <span class="text-[#7519ff] dark:text-[#CBACF9]">approach</span>
    </h2>
    <div class="flex flex-col md:flex-row gap-5 mt-10 md:w-10/12 mx-auto">
      <ApproachCard
        v-for="(approach, index) in approaches"
        :key="index"
        :title="approach.title"
        :subtitle="approach.subtitle"
        :description="approach.description"
      />
    </div>
  </section>
</template>

<script>
import ApproachCard from "./approach/ApproachCard.vue";

export default {
  data() {
    return {
      approaches: {
        first: {
          title: "Research",
          subtitle: "Understanding your needs",
          description:
            "I start by understanding your business goals and target audience to create a tailored solution.",
        },
        second: {
          title: "Design",
          subtitle: "Crafting the user experience",
          description:
            "I design intuitive interfaces that enhance user experience and engagement.",
        },
        third: {
          title: "Development",
          subtitle: "Building the solution",
          description:
            "I develop robust and scalable applications using modern technologies.",
        },
      },
    };
  },
  components: {
    ApproachCard,
  },
};
</script>
