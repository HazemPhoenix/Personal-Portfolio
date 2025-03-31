<template>
  <nav
    class="border-1 border-[#6971A229] text-[#C1C2D3] w-fit rounded-[13px] mx-auto py-5 bg-linear-to-r from-[#04071D] to-[#0C0E23] px-10 flex justify-around gap-7 sticky top-10"
  >
    <a
      href="about"
      class="hover:text-white transition-all"
      :class="{ 'text-white': current === 'about' }"
      >About</a
    >
    <a
      href="projects"
      class="hover:text-white transition-all"
      :class="{ 'text-white': current === 'projects' }"
      >Projects</a
    >
    <a
      href="testimonials"
      class="hover:text-white transition-all"
      :class="{ 'text-white': current === 'testimonials' }"
      >Testimonials</a
    >
    <a
      href="contact"
      class="hover:text-white transition-all"
      :class="{ 'text-white ': current === 'contact' }"
      >Contact</a
    >
  </nav>
</template>

<script>
export default {
  props: {
    current: {
      type: String,
      default: "about",
    },
  },
};
</script>
