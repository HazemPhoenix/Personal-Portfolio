<template>
  <div
    class="relative flex justify-center items-center h-[60vh] border-1 md:w-1/3 border-gray-400 dark:border-[#3637496E] rounded-xl bg-linear-to-r from-gray-80 to-gray-200 dark:from-[#04071D] dark:to-[#0C0E23]"
    id="card-container"
  >
    <div
      class="flex flex-col h-60 justify-between items-center w-11/12 mx-auto"
    >
      <div
        class="flex items-center h-14 border-1 border-[#6971A266] text-[#7519ff] dark:text-[#CBACF9] py-3 px-4 rounded-lg"
      >
        <span class="line-clamp-1">{{ title }}</span>
      </div>
      <div class="h-20 flex items-center">
        <h2 class="text-3xl text-center font-semibold line-clamp-2">
          {{ subtitle }}
        </h2>
      </div>
      <div class="h-24 flex items-center">
        <p class="text-center text-gray-700 dark:text-gray-400 line-clamp-3">
          {{ description }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
#card-container::before,
#card-container::after,
#card-container > div::before,
#card-container > div::after {
  content: "+";
  position: absolute;
  width: 20px;
  height: 20px;
  color: #7519ff;
  font-size: 28px;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: transform 0.3s ease;
}

#card-container::before {
  top: -8px;
  left: -8px;
}

#card-container::after {
  top: -8px;
  right: -8px;
}

#card-container > div::before {
  bottom: -8px;
  left: -8px;
}

#card-container > div::after {
  bottom: -8px;
  right: -8px;
}

#card-container:hover::before {
  transform: rotate(180deg);
}

#card-container:hover::after {
  transform: rotate(-180deg);
}

#card-container:hover > div::before {
  transform: rotate(-180deg);
}

#card-container:hover > div::after {
  transform: rotate(180deg);
}
</style>
