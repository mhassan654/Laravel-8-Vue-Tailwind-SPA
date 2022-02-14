<template>
  <!-- <div class="rounded px-6 py-3 my-2 cursor-pointer transition-all duration-100 ease-in-out group"
       :class="isCurrentRoute ? 'bg-teal-500' : 'bg-transparent hover:bg-gray-100'"
       @click="go"
  >
    <span class="font-semibold transition-all duration-100 ease-in-out" :class="isCurrentRoute ? 'text-white' : 'text-gray-600 group-hover:text-gray-800'">
      <slot />
    </span>
  </div> -->

  <div class="flex items-center p-2 text-base cursor-pointer font-normal text-white rounded-lg dark:text-white
   hover:bg-gray-400 dark:hover:bg-gray-700"
       :class="isCurrentRoute ? 'bg-teal-500' : 'bg-transparent hover:bg-gray-100'"
       @click="go"
  >
    <svg class="w-6 h-6 text-white transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
         fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"
    ><path d="M2 10a8 8 0 018-8v8h8a8 8 0 11-16 0z" /><path d="M12 2.252A8.014 8.014 0 0117.748 8H12V2.252z" /></svg>

    <span class="ml-3" :class="isCurrentRoute ? 'text-white' : 'text-gray-600 group-hover:text-gray-800'">
      <slot />
    </span>
    <!-- </a> -->
  </div>
</template>

<script>
export default {
  name: 'SidebarItem',
  props: {
    route: {
      default: 'dashboard',
      type: String,
      required: true
    }
  },
  computed: {
    isCurrentRoute: function () {
      return this.route === this.$route.name
    }
  },
  methods: {
    go: function () {
      if (!this.isCurrentRoute) {
        this.$router.push({ name: this.route })
      }
    }
  }
}
</script>

<style scoped>

</style>
