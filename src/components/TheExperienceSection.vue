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
          src: "https://scontent.fcai21-2.fna.fbcdn.net/v/t1.15752-9/487003030_826246166390561_4167430245063356735_n.png?stp=cp0_dst-png&_nc_cat=111&ccb=1-7&_nc_sid=9f807c&_nc_ohc=XOD82qUAVtoQ7kNvgFuv7aL&_nc_oc=AdlK-vY7QOvgfUEWr1UPQZwVTuyoquxmANiOIcXHqIs8DpTsE0IEgwh-nZCLGeU_a54&_nc_zt=23&_nc_ht=scontent.fcai21-2.fna&oh=03_Q7cD1wGfczSqvnf_3YlLv8uDZ2B0Lrn_K5l0STT_TFXFoO5_4A&oe=68152F90",
        },
        {
          title: "Full Stack Developer Intern",
          description:
            "Worked on various projects, enhancing skills in both frontend and backend development.",
          src: "https://scontent.fcai21-3.fna.fbcdn.net/v/t1.15752-9/487808529_9615873915144605_1033500959259285034_n.png?_nc_cat=107&ccb=1-7&_nc_sid=9f807c&_nc_ohc=exWKeROTsw4Q7kNvgGlczrL&_nc_oc=Adl6BaRXmlvPm0jz5JhnOoyR-UNe4XYcODC4iBZ-U4ZgsIyD-f_VmIdB4tIMSMXLfz8&_nc_zt=23&_nc_ht=scontent.fcai21-3.fna&oh=03_Q7cD1wGqqYO8zLYsPvOvjeA3zAODwk1vW_ye4uLkfoeWmvmeZg&oe=681545B4",
        },
        {
          title: "Backend Java Developer Intern",
          description:
            "Developed backend solutions using Java and Spring Boot.",
          src: "https://scontent.fcai21-2.fna.fbcdn.net/v/t1.15752-9/488039573_591217083965554_5963000751818606823_n.png?stp=cp0_dst-png&_nc_cat=106&ccb=1-7&_nc_sid=9f807c&_nc_ohc=Qm_ULD9wGBYQ7kNvgHp-dwn&_nc_oc=Adl_F-LGf1Wa_B2AJi5Lf513Xd9IjJqjTSx1hx_VQUCvAerEvzsKLWdO9A7krVcVggs&_nc_zt=23&_nc_ht=scontent.fcai21-2.fna&oh=03_Q7cD1wFptPY6_aHcZpn2jPG-J4p9gijZPfj5cReRwUTO_R7IqA&oe=681539D3",
        },
        {
          title: "Backend Java Developer",
          description:
            "Contributed to backend development projects, focusing on Java and Spring Boot.",
          src: "https://scontent.fcai21-4.fna.fbcdn.net/v/t1.15752-9/487033336_2387346624972462_7061184434550039657_n.png?_nc_cat=102&ccb=1-7&_nc_sid=9f807c&_nc_ohc=KHLdfp8-0HYQ7kNvgHrhcGj&_nc_oc=AdnZYC-Uqm6E7hOb-6k15krMwRx5qxUh8VsIQSCqEOYJEur26qgPvKz7Ewg0JPgFzBE&_nc_zt=23&_nc_ht=scontent.fcai21-4.fna&oh=03_Q7cD1wEalbhD6brdbHC2PklRy4Grffas5FGpLc0NHz6VJdgAvw&oe=68153D8A",
        },
      ],
    };
  },
  components: {
    ExperienceCard,
  },
};
</script>
