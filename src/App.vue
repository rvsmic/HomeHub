<template>
  <div
    class="title-font xl:text-9xl lg:text-8xl md:text-7xl sm:text-6xl text-5xl uppercase text-center w-full py-5 text-light-accent-1 dark:text-dark-accent-1 mt-10"
  >
    HOMEHUB
  </div>
  <div
    class="2xl:mx-96 xl:mx-60 lg:mx-40 md:mx-20 sm:mx-10 md:my-10 sm:my-5 grid grid-cols-2 mb-40"
  >
    <ServiceButton
      v-for="link in links"
      :key="link.title"
      :title="link.title"
      :url="link.url"
      :svg="link.svg"
    >
    </ServiceButton>
  </div>
</template>

<script>
import ServiceButton from './components/ServiceButton.vue'

export default {
  components: {
    ServiceButton,
  },
  computed: {
    links() {
      // https://www.svgrepo.com/collection/dazzle-line-icons/
      return [
        {
          title: 'Portfolio',
          url: 'https://rvsmic.github.io',
          svg: 'M16 7C16 9.20914 14.2091 11 12 11C9.79086 11 8 9.20914 8 7C8 4.79086 9.79086 3 12 3C14.2091 3 16 4.79086 16 7Z M12 14C8.13401 14 5 17.134 5 21H19C19 17.134 15.866 14 12 14Z',
        },
        {
          title: 'Przepisowo',
          url: 'https://rvsmic.duckdns.org:60001',
          svg: 'M8 21V3M15 21V3C17.2091 3 19 4.79086 19 7V9C19 11.2091 17.2091 13 15 13M11 3V8C11 9.65685 9.65685 11 8 11C6.34315 11 5 9.65685 5 8V3',
        },
        {
          title: 'Nespresso',
          url: 'https://rvsmic.duckdns.org:60002',
          svg: 'M18.5 7H19C19.4647 7 19.697 7 19.8902 7.03843C20.6836 7.19624 21.3038 7.81644 21.4616 8.60982C21.5 8.80302 21.5 9.03535 21.5 9.5C21.5 9.96465 21.5 10.197 21.4616 10.3902C21.3038 11.1836 20.6836 11.8038 19.8902 11.9616C19.697 12 19.4647 12 19 12H18.5M3 20H21M12 17C10.6055 17 9.90821 17 9.33277 16.8619C7.50453 16.4229 6.07707 14.9955 5.63815 13.1672C5.5 12.5918 5.5 11.8945 5.5 10.5L5.5 7.2C5.5 6.0799 5.5 5.51984 5.71799 5.09202C5.90973 4.7157 6.21569 4.40974 6.59202 4.21799C7.01984 4 7.57989 4 8.7 4L15.3 4C16.4201 4 16.9802 4 17.408 4.21799C17.7843 4.40973 18.0903 4.71569 18.282 5.09202C18.5 5.51984 18.5 6.07989 18.5 7.2V10.5C18.5 11.8945 18.5 12.5918 18.3619 13.1672C17.9229 14.9955 16.4955 16.4229 14.6672 16.8619C14.0918 17 13.3945 17 12 17Z',
        },
      ]
    },
  },
}
</script>
