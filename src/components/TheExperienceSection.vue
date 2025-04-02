<template>
  <section class="mt-10">
    <h2 class="text-center text-2xl md:text-5xl font-bold">
      My
      <span class="text-[#7519ff] dark:text-[#CBACF9]">work experience</span>
    </h2>
    <div class="grid md:grid-cols-2 gap-5 md:w-10/12 mx-auto mt-15">
      <ExperienceCard
        v-for="(experience, index) in experiences"
        :key="index"
        :src="experience.src"
        :title="experience.title"
        :description="experience.description"
      />
    </div>
  </section>
</template>

<script>
import ExperienceCard from "./experience/ExperienceCard.vue";

export default {
  data() {
    return {
      experiences: [
        {
          title: "Frontend Trainee",
          description:
            "Gained hands-on experience in frontend technologies and frameworks.",
          src: "../../assets/svg/experience/_Group_.svg",
        },
        {
          title: "Full Stack Developer Intern",
          description:
            "Worked on various projects, enhancing skills in both frontend and backend development.",
          src: "../../assets/svg/experience/_Group_-1.svg",
        },
        {
          title: "Backend Java Developer Intern",
          description:
            "Developed backend solutions using Java and Spring Boot.",
          src: "../../assets/svg/experience/Frame 5.svg",
        },
        {
          title: "Backend Java Developer",
          description:
            "Contributed to backend development projects, focusing on Java and Spring Boot.",
          src: "../../assets/svg/experience/Rectangle.svg",
        },
      ],
    };
  },
  components: {
    ExperienceCard,
  },
};
</script>
