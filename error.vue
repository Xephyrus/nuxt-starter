<script setup lang="ts">
import type { NuxtError } from "#app";

const props = defineProps({
  error: Object as () => NuxtError,
});
</script>

<template>
  <Head>
    <link href="https://fonts.cdnfonts.com/css/lcd" rel="stylesheet" />
  </Head>
  <!-- <div class="error-page">
    <h1>{{ error?.statusCode }}</h1>
    <NuxtLink to="/">Go back home</NuxtLink>
  </div> -->
  <main
    class="grid min-h-full place-items-center bg-white px-6 py-24 sm:py-32 lg:px-8"
  >
    <div class="text-center">
      <p class="text-5xl font-semibold text-indigo-600 font-lcd">
        {{ error?.statusCode }}
      </p>
      <h1
        class="mt-4 text-5xl font-semibold tracking-tight text-balance text-gray-900 sm:text-7xl"
      >
        {{ error?.message }}
      </h1>
      <pre
        class="mt-6 text-lg font-medium text-pretty text-gray-500 sm:text-xl/8"
      >
        Sorry, we couldn’t find the page you’re looking for.
      </pre>
      <div class="mt-10 flex items-center justify-center gap-x-6">
        <NuxtLink
          to="/"
          class="font-lcd text-2xl rounded-md bg-indigo-600 px-3.5 py-2.5 font-semibold text-white shadow-xs hover:bg-indigo-500 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
          >Go back home</NuxtLink
        >
        <button
          class="font-lcd text-2xl rounded-md px-3.5 py-2.5 font-semibold text-gray-900 bg-gray-200 hover:bg-gray-100 cursor-pointer"
          @click="$router.go(-1)"
        >
          Or, back to previous page <span aria-hidden="true">&rarr;</span>
        </button>
      </div>
    </div>
  </main>
</template>

<style scoped>
.font-lcd {
  font-family: "LCD", sans-serif;
}
</style>
