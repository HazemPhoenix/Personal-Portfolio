<template>
  <section class="mt-20 flex flex-col gap-5 md:gap-10" id="projects">
    <h2 class="text-center text-2xl md:text-5xl font-bold">
      A small selection of
      <span class="text-[#7519ff] dark:text-[#CBACF9]">recent projects</span>
    </h2>
    <div class="grid md:grid-cols-2 gap-5 md:w-11/12 md:mx-auto">
      <ProjectCard
        v-for="(project, index) in projects"
        :key="index"
        :src="project.imageUrl"
        :alt="project.title"
        :title="project.title"
        :description="project.description"
        :link="project.link"
        :technologies="project.technologies"
      />
    </div>
  </section>
</template>

<script>
import ProjectCard from "./RecentProjects/ProjectCard.vue";

export default {
  data() {
    return {
      projects: [
        {
          title: "Reservio",
          description:
            "Reservio is a web app that connects venue owners with customers seeking event spaces, enabling venue searches, availability checks, and online reservations.",
          imageUrl: "../../../public/images/projects/reservio.png",
          link: "https://reservio-two.vercel.app/",
          technologies: {
            vue: "../../../public/svg/vue.svg",
            tailwind: "../../../public/svg/tailwind.svg",
            firebase: "../../../public/svg/firebase.svg",
            express: "../../../public/svg/express.svg",
          },
        },
        {
          title: "Reservio",
          description:
            "Reservio is a web app that connects venue owners with customers seeking event spaces, enabling venue searches, availability checks, and online reservations.",
          imageUrl: "../../../public/images/projects/reservio.png",
          link: "https://reservio-two.vercel.app/",
          technologies: {
            vue: "../../../public/svg/vue.svg",
            tailwind: "../../../public/svg/tailwind.svg",
            firebase: "../../../public/svg/firebase.svg",
            express: "../../../public/svg/express.svg",
          },
        },
        {
          title: "Reservio",
          description:
            "Reservio is a web app that connects venue owners with customers seeking event spaces, enabling venue searches, availability checks, and online reservations.",
          imageUrl: "../../../public/images/projects/reservio.png",
          link: "https://reservio-two.vercel.app/",
          technologies: {
            vue: "../../../public/svg/vue.svg",
            tailwind: "../../../public/svg/tailwind.svg",
            firebase: "../../../public/svg/firebase.svg",
            express: "../../../public/svg/express.svg",
          },
        },
        {
          title: "Reservio",
          description:
            "Reservio is a web app that connects venue owners with customers seeking event spaces, enabling venue searches, availability checks, and online reservations.",
          imageUrl: "../../../public/images/projects/reservio.png",
          link: "https://reservio-two.vercel.app/",
          technologies: {
            vue: "../../../public/svg/vue.svg",
            tailwind: "../../../public/svg/tailwind.svg",
            firebase: "../../../public/svg/firebase.svg",
            express: "../../../public/svg/express.svg",
          },
        },
      ],
    };
  },
  components: {
    ProjectCard,
  },
};
</script>
