<template>
  <header
    class="md:h-[100vh] md:w-9/12 mx-auto mt-32 md:mt-52 text-center dark:text-white text-gray-800"
  >
    <p
      class="text-sm tracking-widest dark:text-gray-400 text-gray-800 uppercase"
    >
      Dynamic Web Magic with Vue.js and Laravel
    </p>
    <h1 class="text-3xl md:text-6xl font-bold mt-4">
      Transforming Concepts into Seamless
      <span class="dark:text-[#CBACF9] text-[#7519ff]">User Experiences</span>
    </h1>
    <p class="text-lg dark:text-gray-400 text-gray-800 mt-4">
      Hi! I'm <span class="font-semibold">Hazem Abdulmoneim</span>, a
      Laravel/Vue.js Developer based in Egypt
    </p>
    <a href="https://github.com/HazemPhoenix" target="_blank">
      <BaseButton class="w-full md:w-auto">
        See my work
        <img src="../assets/svg/Arrow.svg" alt="" class="ps-2" />
      </BaseButton>
    </a>
  </header>
</template>

<script>
import BaseButton from "./base/BaseButton.vue";

export default {};
</script>
