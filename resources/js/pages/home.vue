<template>
  <div class="max-w-7xl mx-auto py-6 sm:px-6 lg:px-8">
    <h1 class="text-2xl font-bold text-gray-400 m-auto leading-none select-none text-center">
      <div class="px-4 py-6 sm:px-0" />
      <div class="flex flex-row md:flex-row">
        <div class="p-6 max-w-sm bg-dark rounded-lg border border-gray-200 shadow-md dark:bg-gray-800 dark:bg-gray-700">
          <a href="#">
            <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Noteworthy technology acquisitions 2021</h5>
          </a>
          <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
            card 1
          </p>
        </div>

        <div class="p-6 max-w-sm bg-p rounded-lg border border-gray-200 shadow-md dark:bg-gray-800 dark:bg-gray-700">
          <a href="#">
            <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
              card 2</h5>
          </a>
          <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
            Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
          </p>
        </div>
      </div>
    </h1>
  </div>
</template>

<script>
export default {
  middleware: 'auth',

  metaInfo () {
    return { title: this.$t('home') }
  }
}
</script>
