<template>
  <main
    class="grid md:grid-cols-5 md:grid-rows-4 gap-6 mt-20 md:mt-0 text-white dark:bg-[#000319]"
  >
    <div
      class="h-[30vh] md:h-[64vh] bg-[url(../assets/images/laptop.png)] bg-cover rounded-[23px] md:col-span-3 md:row-span-2"
    >
      <h2
        class="w-8/12 md:w-7/12 text-xl md:text-3xl font-bold ms-5 md:ms-10 relative top-3/5 md:top-4/6"
      >
        I prioritize client collaboration, fostering open communication
      </h2>
    </div>
    <div
      class="h-[15vh] md:h-[30vh] bg-[url(../assets/images/world-map.png)] bg-cover rounded-[23px] md:col-span-2 md:row-span-1"
    >
      <h2 class="text-xl md:text-3xl font-bold relative top-10 left-10">
        I'm very flexible with time zone communications
      </h2>
    </div>
    <div
      class="h-[20vh] md:h-[30vh] bg-[url(../assets/svg/skills.svg)] bg-right bg-cover rounded-[23px] md:col-span-2 md:row-span-1"
    >
      <div class="relative top-16 left-2 md:top-20 md:left-10">
        <p class="text-xs md:text-lg text-gray-400">
          I constantly try to improve
        </p>
        <h2 class="text-2xl md:text-4xl">My tech stack</h2>
      </div>
    </div>
    <div
      class="h-[15vh] md:h-[30vh] bg-[url(../assets/svg/passion.svg)] bg-cover bg-bottom rounded-[23px] md:col-span-2 md:row-span-1"
      id="passion"
    >
      <h2 class="relative top-5 md:top-10 left-5 text-xl font-bold w-11/12">
        Tech enthusiast with a passion for development.
      </h2>
    </div>
    <div
      class="h-[20vh] md:h-[64vh] bg-[#00061e] rounded-[23px] md:col-span-3 md:row-span-3 relative flex"
    >
      <div class="w-full relative z-50 flex flex-col justify-center ps-5">
        <p class="text-xs md:text-lg uppercase tracking-wider text-gray-400">
          The Inside Scoop
        </p>
        <h2 class="text-lg md:text-4xl font-semibold">
          Currently studying full-stack PHP/Laravel Development
        </h2>
      </div>
      <div class="w-full relative right-0">
        <div
          class="absolute inset-0 z-30 bg-[url(../assets/images/code.png)] bg-cover bg-no-repeat bg-left"
        ></div>
      </div>
      <div
        class="absolute opacity-20 inset-0 z-20"
        style="
          background: radial-gradient(
            circle at center,
            #1e40af 0%,
            #06091f 50%
          );
        "
      ></div>
    </div>
    <div
      class="h-[18vh] md:h-[30vh] rounded-[23px] md:col-span-2 md:row-span-1 flex justify-center items-center relative overflow-hidden"
      style="
        background: radial-gradient(
          circle at bottom left,
          pink 0%,
          #1e40af 20%,
          #06091f 55%
        );
      "
    >
      <div
        class="absolute inset-0 backdrop-blur-[15px] bg-[#06091F]/50 animate-pulse"
      ></div>
      <div class="w-10/12 md:w-11/12 text-center relative z-10">
        <h2 class="text-xl md:text-2xl font-bold">
          Do you want to start a project together?
        </h2>
        <BaseButton
          @click="copyEmail"
          class="flex gap-3 h-[38px] md:h-[41px] text-sm w-fit md:w-8/12"
        >
          <img src="../assets/svg/Card.svg" />
          Copy my email address
        </BaseButton>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  methods: {
    copyEmail() {
      navigator.clipboard.writeText("hazemabdulmoneim@gmail.com");
      alert("Email copied to clipboard!");
    },
  },
};
</script>
