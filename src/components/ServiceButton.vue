<template>
  <a :href="url">
    <div
      class="bg-light-accent-3 dark:bg-dark-accent-3 mx-5 my-5 sm:px-10 py-5 rounded-2xl text-center lg:text-3xl md:text-xl sm:text-lg text-base hover:scale-105 transform transition duration-150 stroke-light-accent-1 dark:stroke-dark-accent-1 hover:stroke-light-accent-2 hover:dark:stroke-dark-accent-2 active:scale-105 active:stroke-light-accent-2 active:dark:stroke-dark-accent-2"
    >
      <svg
        class="xl:h-60 lg:h-50 md:h-40 sm:h-30 h-15 m-auto"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
        <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
        <g id="SVGRepo_iconCarrier">
          <path :d="svg" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path>
        </g>
      </svg>
      {{ title }}
    </div>
  </a>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    url: {
      type: String,
      required: true,
    },
    svg: {
      type: String,
      required: false,
    },
  },
}
</script>
