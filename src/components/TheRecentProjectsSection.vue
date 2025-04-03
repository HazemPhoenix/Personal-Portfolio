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
          imageUrl:
            "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/488077064_23935753379364246_8367150981750435219_n.png?_nc_cat=104&ccb=1-7&_nc_sid=9f807c&_nc_ohc=dBMyjVhvVeQQ7kNvgEtDo1U&_nc_oc=AdlMYmJGi9t-UlEe933TBwe_VdM6OSAKEtrtzonY4lHVkMm452TV1Zhvan-Ne83Z1DA&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wHsImWkarCKAEbsWVBWS-SfrCat78kHJgzSzWGKU_HFsw&oe=68155463",
          link: "https://reservio-two.vercel.app/",
          technologies: [
            "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/486781360_1303311174088590_6966199852792008879_n.png?_nc_cat=104&ccb=1-7&_nc_sid=9f807c&_nc_ohc=Pk-EL0qQMdYQ7kNvgHLSigq&_nc_oc=AdmFakbOLc3EWyF03_0cYhlUOhRRWiFQA0jsZy8RekTySXHzkkCyW3f2MlYbJlNZOTc&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wGksHHYR1nZZxuMW1L0UZZBfo--R3gRiKzk9YXepIX5fA&oe=681547B6",
            "https://scontent.fcai21-3.fna.fbcdn.net/v/t1.15752-9/486768486_1043189177631572_3010795599089243332_n.png?_nc_cat=108&ccb=1-7&_nc_sid=9f807c&_nc_ohc=YjUKo3dGQNMQ7kNvgEydIw7&_nc_oc=Adn2lQpLb22ePFzvaSS4K1q-RhG2zjgZabOg_5KkCncC3zUZKt5fA8YmVgYrJnDPfFk&_nc_zt=23&_nc_ht=scontent.fcai21-3.fna&oh=03_Q7cD1wEviP8ieKl6YTDAv3vPtkY4es4B-unCrinxa9RdmDgo4Q&oe=681555FE",
            "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/487081260_677272914811847_2141142011204743290_n.png?_nc_cat=102&ccb=1-7&_nc_sid=9f807c&_nc_ohc=XyPhF67Ibv8Q7kNvgE9rExX&_nc_oc=AdkD8Xxvil2kmQO3yaJI91voR3MZzfwhKwUeqY1MtjqMBGQgpDpQ4Ve6SSHMIGHw5LQ&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wHZ3X9vkyCoG1XOtSYex1FaW2HkeCVwSspj9AXUkxcKHA&oe=68154F3C",
            "https://scontent.fcai21-3.fna.fbcdn.net/v/t1.15752-9/487835247_1416050262891019_9216655942687731363_n.png?_nc_cat=100&ccb=1-7&_nc_sid=9f807c&_nc_ohc=O8YcxUbspQcQ7kNvgHQsceB&_nc_oc=Adl8iX8v9ZbrJ2IJyC2Tw-xdL-77nT1AQdJVqmwmiYB5sGyCHfbV7pkbFHCCMRLpRkw&_nc_zt=23&_nc_ht=scontent.fcai21-3.fna&oh=03_Q7cD1wGfaKrNQIlt22Hk7BrKzzREgG4JGzKYNmty80CAJT22WA&oe=68154FFE",
          ],
        },
        {
          title: "Reservio",
          description:
            "Reservio is a web app that connects venue owners with customers seeking event spaces, enabling venue searches, availability checks, and online reservations.",
          imageUrl:
            "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/488077064_23935753379364246_8367150981750435219_n.png?_nc_cat=104&ccb=1-7&_nc_sid=9f807c&_nc_ohc=dBMyjVhvVeQQ7kNvgEtDo1U&_nc_oc=AdlMYmJGi9t-UlEe933TBwe_VdM6OSAKEtrtzonY4lHVkMm452TV1Zhvan-Ne83Z1DA&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wHsImWkarCKAEbsWVBWS-SfrCat78kHJgzSzWGKU_HFsw&oe=68155463",
          link: "https://reservio-two.vercel.app/",
          technologies: [
            "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/486781360_1303311174088590_6966199852792008879_n.png?_nc_cat=104&ccb=1-7&_nc_sid=9f807c&_nc_ohc=Pk-EL0qQMdYQ7kNvgHLSigq&_nc_oc=AdmFakbOLc3EWyF03_0cYhlUOhRRWiFQA0jsZy8RekTySXHzkkCyW3f2MlYbJlNZOTc&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wGksHHYR1nZZxuMW1L0UZZBfo--R3gRiKzk9YXepIX5fA&oe=681547B6",
            "https://scontent.fcai21-3.fna.fbcdn.net/v/t1.15752-9/486768486_1043189177631572_3010795599089243332_n.png?_nc_cat=108&ccb=1-7&_nc_sid=9f807c&_nc_ohc=YjUKo3dGQNMQ7kNvgEydIw7&_nc_oc=Adn2lQpLb22ePFzvaSS4K1q-RhG2zjgZabOg_5KkCncC3zUZKt5fA8YmVgYrJnDPfFk&_nc_zt=23&_nc_ht=scontent.fcai21-3.fna&oh=03_Q7cD1wEviP8ieKl6YTDAv3vPtkY4es4B-unCrinxa9RdmDgo4Q&oe=681555FE",
            "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/487081260_677272914811847_2141142011204743290_n.png?_nc_cat=102&ccb=1-7&_nc_sid=9f807c&_nc_ohc=XyPhF67Ibv8Q7kNvgE9rExX&_nc_oc=AdkD8Xxvil2kmQO3yaJI91voR3MZzfwhKwUeqY1MtjqMBGQgpDpQ4Ve6SSHMIGHw5LQ&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wHZ3X9vkyCoG1XOtSYex1FaW2HkeCVwSspj9AXUkxcKHA&oe=68154F3C",
            "https://scontent.fcai21-3.fna.fbcdn.net/v/t1.15752-9/487835247_1416050262891019_9216655942687731363_n.png?_nc_cat=100&ccb=1-7&_nc_sid=9f807c&_nc_ohc=O8YcxUbspQcQ7kNvgHQsceB&_nc_oc=Adl8iX8v9ZbrJ2IJyC2Tw-xdL-77nT1AQdJVqmwmiYB5sGyCHfbV7pkbFHCCMRLpRkw&_nc_zt=23&_nc_ht=scontent.fcai21-3.fna&oh=03_Q7cD1wGfaKrNQIlt22Hk7BrKzzREgG4JGzKYNmty80CAJT22WA&oe=68154FFE",
          ],
        },
        {
          title: "Reservio",
          description:
            "Reservio is a web app that connects venue owners with customers seeking event spaces, enabling venue searches, availability checks, and online reservations.",
          imageUrl:
            "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/488077064_23935753379364246_8367150981750435219_n.png?_nc_cat=104&ccb=1-7&_nc_sid=9f807c&_nc_ohc=dBMyjVhvVeQQ7kNvgEtDo1U&_nc_oc=AdlMYmJGi9t-UlEe933TBwe_VdM6OSAKEtrtzonY4lHVkMm452TV1Zhvan-Ne83Z1DA&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wHsImWkarCKAEbsWVBWS-SfrCat78kHJgzSzWGKU_HFsw&oe=68155463",
          link: "https://reservio-two.vercel.app/",
          technologies: [
            "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/486781360_1303311174088590_6966199852792008879_n.png?_nc_cat=104&ccb=1-7&_nc_sid=9f807c&_nc_ohc=Pk-EL0qQMdYQ7kNvgHLSigq&_nc_oc=AdmFakbOLc3EWyF03_0cYhlUOhRRWiFQA0jsZy8RekTySXHzkkCyW3f2MlYbJlNZOTc&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wGksHHYR1nZZxuMW1L0UZZBfo--R3gRiKzk9YXepIX5fA&oe=681547B6",
            "https://scontent.fcai21-3.fna.fbcdn.net/v/t1.15752-9/486768486_1043189177631572_3010795599089243332_n.png?_nc_cat=108&ccb=1-7&_nc_sid=9f807c&_nc_ohc=YjUKo3dGQNMQ7kNvgEydIw7&_nc_oc=Adn2lQpLb22ePFzvaSS4K1q-RhG2zjgZabOg_5KkCncC3zUZKt5fA8YmVgYrJnDPfFk&_nc_zt=23&_nc_ht=scontent.fcai21-3.fna&oh=03_Q7cD1wEviP8ieKl6YTDAv3vPtkY4es4B-unCrinxa9RdmDgo4Q&oe=681555FE",
            "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/487081260_677272914811847_2141142011204743290_n.png?_nc_cat=102&ccb=1-7&_nc_sid=9f807c&_nc_ohc=XyPhF67Ibv8Q7kNvgE9rExX&_nc_oc=AdkD8Xxvil2kmQO3yaJI91voR3MZzfwhKwUeqY1MtjqMBGQgpDpQ4Ve6SSHMIGHw5LQ&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wHZ3X9vkyCoG1XOtSYex1FaW2HkeCVwSspj9AXUkxcKHA&oe=68154F3C",
            "https://scontent.fcai21-3.fna.fbcdn.net/v/t1.15752-9/487835247_1416050262891019_9216655942687731363_n.png?_nc_cat=100&ccb=1-7&_nc_sid=9f807c&_nc_ohc=O8YcxUbspQcQ7kNvgHQsceB&_nc_oc=Adl8iX8v9ZbrJ2IJyC2Tw-xdL-77nT1AQdJVqmwmiYB5sGyCHfbV7pkbFHCCMRLpRkw&_nc_zt=23&_nc_ht=scontent.fcai21-3.fna&oh=03_Q7cD1wGfaKrNQIlt22Hk7BrKzzREgG4JGzKYNmty80CAJT22WA&oe=68154FFE",
          ],
        },
        {
          title: "Reservio",
          description:
            "Reservio is a web app that connects venue owners with customers seeking event spaces, enabling venue searches, availability checks, and online reservations.",
          imageUrl:
            "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/488077064_23935753379364246_8367150981750435219_n.png?_nc_cat=104&ccb=1-7&_nc_sid=9f807c&_nc_ohc=dBMyjVhvVeQQ7kNvgEtDo1U&_nc_oc=AdlMYmJGi9t-UlEe933TBwe_VdM6OSAKEtrtzonY4lHVkMm452TV1Zhvan-Ne83Z1DA&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wHsImWkarCKAEbsWVBWS-SfrCat78kHJgzSzWGKU_HFsw&oe=68155463",
          link: "https://reservio-two.vercel.app/",
          technologies: [
            "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/486781360_1303311174088590_6966199852792008879_n.png?_nc_cat=104&ccb=1-7&_nc_sid=9f807c&_nc_ohc=Pk-EL0qQMdYQ7kNvgHLSigq&_nc_oc=AdmFakbOLc3EWyF03_0cYhlUOhRRWiFQA0jsZy8RekTySXHzkkCyW3f2MlYbJlNZOTc&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wGksHHYR1nZZxuMW1L0UZZBfo--R3gRiKzk9YXepIX5fA&oe=681547B6",
            "https://scontent.fcai21-3.fna.fbcdn.net/v/t1.15752-9/486768486_1043189177631572_3010795599089243332_n.png?_nc_cat=108&ccb=1-7&_nc_sid=9f807c&_nc_ohc=YjUKo3dGQNMQ7kNvgEydIw7&_nc_oc=Adn2lQpLb22ePFzvaSS4K1q-RhG2zjgZabOg_5KkCncC3zUZKt5fA8YmVgYrJnDPfFk&_nc_zt=23&_nc_ht=scontent.fcai21-3.fna&oh=03_Q7cD1wEviP8ieKl6YTDAv3vPtkY4es4B-unCrinxa9RdmDgo4Q&oe=681555FE",
            "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/487081260_677272914811847_2141142011204743290_n.png?_nc_cat=102&ccb=1-7&_nc_sid=9f807c&_nc_ohc=XyPhF67Ibv8Q7kNvgE9rExX&_nc_oc=AdkD8Xxvil2kmQO3yaJI91voR3MZzfwhKwUeqY1MtjqMBGQgpDpQ4Ve6SSHMIGHw5LQ&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wHZ3X9vkyCoG1XOtSYex1FaW2HkeCVwSspj9AXUkxcKHA&oe=68154F3C",
            "https://scontent.fcai21-3.fna.fbcdn.net/v/t1.15752-9/487835247_1416050262891019_9216655942687731363_n.png?_nc_cat=100&ccb=1-7&_nc_sid=9f807c&_nc_ohc=O8YcxUbspQcQ7kNvgHQsceB&_nc_oc=Adl8iX8v9ZbrJ2IJyC2Tw-xdL-77nT1AQdJVqmwmiYB5sGyCHfbV7pkbFHCCMRLpRkw&_nc_zt=23&_nc_ht=scontent.fcai21-3.fna&oh=03_Q7cD1wGfaKrNQIlt22Hk7BrKzzREgG4JGzKYNmty80CAJT22WA&oe=68154FFE",
          ],
        },
      ],
    };
  },
  components: {
    ProjectCard,
  },
};
</script>
