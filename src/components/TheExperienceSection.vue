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
          src: "https://d23j1yojw6x37d.cloudfront.net/w1jyp7%2Fpreview%2F65865259%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632593&Signature=JANH-zBaEkmoFFqaHP6H4~XKqlpeFu7OYD4xlpPnoLnf36F7lU2c1d-LKuR9OOAakM8Mu0HA6toeu968-~m4gsqMYrTQnvjFHIugkY1q~VgbunzOr9z-v2MYLLueP3TCvNPtDoTEeAShlAzzSVQg-5iPbmQpAPKg7rapEQckehKWRBf4jWyA-SBeEt5C2dSLsMSUINtOYBI48yDtpFf7AFmeQiqWkkjS5bKkcevqRIT-m9k7xcoKC~bV1m3y7XoY5-sejm4i3orSKirtk2Nv7HN9OHGIhmUzmo~d5WuWPCMyCLm2K1BRrSTmxlMDeAa5LysvU9BGp3hgaR2-N2ADZw__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
        },
        {
          title: "Full Stack Developer Intern",
          description:
            "Worked on various projects, enhancing skills in both frontend and backend development.",
          src: "https://dxnxre0ffcj8a.cloudfront.net/z4gvp7%2Fpreview%2F65865148%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632618&Signature=Zb1~~1KZrogJEHSepWE~~rwZ8KIzDpy~lWpvgjcokv15rJdz6-dR2uyME3ClS1t2S7Na9TcUUsfv8l2Pw4qG6qPUh~d266utelYGe5zZQZLfE8QoMGlGgDh3a4talpigKVQq3y-SaE1zDNbi6kMLZ8l-or6NkrXTGRDnNXi2LKLJlX1yqqtZQGJegNmsC55N657clOm1zstSzyOnJp4X0zYvjW0VWj0XN~0acMTMoF2yUY4iHfMvPLgZrUgfgmzhrL2VIHj8wAo5I-axNcC3o~mOIHGZd~KVpPJeoHFrpSHbtCq7pcrlz1YfB~9CGppdvg2azrXp5tkY22rU5xDmbQ__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
        },
        {
          title: "Backend Java Developer Intern",
          description:
            "Developed backend solutions using Java and Spring Boot.",
          src: "https://d2a0js77mxcrjd.cloudfront.net/b96xp7%2Fpreview%2F65865210%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632634&Signature=H2irOygIWRZ-k7p-6Zy2TA-uU8uOI74RCTNswOeqqbGZVmN3WtVN7rgjW3GddbHBIC63jO7LVhLtdKsv-oU2tgxSgJw-Uyhj2Ac99s6mDGc2rRwmK8QMby2Ndnv5Xvaqf8G1GQdgN598Kgjgird5adMszOenHfwshp7qkGEDOAkqfNm7wGFyima6aI0IGVUS7oyf9agksDs~gigzSoEKQYUDPd68CZwvSB8Fc2N7eKZlJFCtWnOVE4Wc4A18NDSxsdzNTQ6uRSWOn8yj9Zdp1tJjKHmLHwKPaZIEiPMgwy81Fk4ptH53om-phPjvAO5V0PSVQinoL~BLBfkV0qEQ~g__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
        },
        {
          title: "Backend Java Developer",
          description:
            "Contributed to backend development projects, focusing on Java and Spring Boot.",
          src: "https://d142ifyzxiteda.cloudfront.net/s3gpp7%2Fpreview%2F65864932%2Fmain_large.png?response-content-disposition=inline%3Bfilename%3D%22main_large.png%22%3B&response-content-type=image%2Fpng&Expires=1743632652&Signature=K5jUjL8jpepvxa1CgXNzmtMN1tj5mLD~ZEK9QNuK7~aRnXe-1avIEb-eCd3eiNnRXVS2IxhVR379xPg1-v~u9WxaEuRDfin1mTfvPOxpWLXO~VpaSC6LnPDwoxvhGsxlr43LtbY29jVQjDYzNRKsu~PAVrD7wQf3x7F~4PZDK2HilGJZ1~CPUA1eUbjVSaQ1~ept7C3ptoewFdW2Bff9UT4adQFRdkwSa8iDX4AOdUfbo2zsZSftQ5eC6Ml-N5xMq-RNKz88IbJeK463ofN20Xte-FuHY5O5B29yWMWkyHsC9ShDqbWxc6JRoK6CfDxo7mbXqwSVHuSV6BjaQsSp7w__&Key-Pair-Id=APKAJT5WQLLEOADKLHBQ",
        },
      ],
    };
  },
  components: {
    ExperienceCard,
  },
};
</script>
