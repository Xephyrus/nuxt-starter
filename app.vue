<script setup>
useHead({
  htmlAttrs: { lang: "zh-CN" },
  title: "Nuxt Starter",
  meta: [
    {
      name: "description",
      content:
        "Nuxt Starter is a minimal template created for quick landing pages, built with Nuxt and Tailwind CSS.",
    },
  ],
  bodyAttrs: {
    class: 'font-display'
  }
});
</script>

<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
