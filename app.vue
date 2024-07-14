<script setup lang="ts">
useHead({
  title: "KangJono",
  htmlAttrs: {
    lang: "en",
  },
  meta: [
    { charset: "UTF-8" },
    { name: "viewport", content: "width=device-width, initial-scale=1.0" },
    {
      name: "description",
      content: "A portfolio built with Nuxt 3 and Tailwind CSS.",
    },
    {
      name: "keywords",
      content: "portfolio, Nuxt 3, Tailwind CSS, web development, customization",
    },
    { name: "author", content: "Jono" },
    { property: "og:type", content: "website" },
    { property: "og:url", content: "https://kangjono-portfolio.vercel.app/" },
    {
      property: "og:title",
      content: "Portfolio with Nuxt & Tailwind CSS",
    },
    {
      property: "og:image",
      content: "https://cdn.sazumi.moe/file/k5chq4.png",
    },
    {
      property: "og:description",
      content: "A built with Nuxt 3 and Tailwind CSS.",
    },

    {
      property: "twitter:card",
      content: "https://cdn.sazumi.moe/file/k5chq4.png",
    },
    {
      property: "twitter:url",
      content: "https://kangjono-portfolio.vercel.app/",
    },
    {
      property: "twitter:title",
      content: "Portfolio with Nuxt & Tailwind CSS",
    },
    {
      property: "twitter:description",
      content: "A portfolio built with Nuxt and Tailwind CSS.",
    },
  ],
  link: [{ rel: "icon", type: "image/png", href: "/favicon.ico" }],
});
</script>

<template>
  <NuxtLayout>
    <Suspense>
      <Pageloader />
    </Suspense>
    <NuxtPage />
  </NuxtLayout>
</template>

<style></style>
