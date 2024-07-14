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
      content: "A customizable portfolio template built with Nuxt 3 and Tailwind CSS. Easy to set up and perfect for showcasing your skills and experience.",
    },
    {
      name: "keywords",
      content: "portfolio template, Nuxt 3, Tailwind CSS, web development, customization",
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
      content: "https://i0.wp.com/curiositygym.com/wp-content/uploads/2022/05/portfolio1.jpg?fit=1920%2C1080&ssl=1",
    },
    {
      property: "og:description",
      content: "A built with Nuxt 3 and Tailwind CSS.",
    },

    {
      property: "twitter:card",
      content: "https://i0.wp.com/curiositygym.com/wp-content/uploads/2022/05/portfolio1.jpg?fit=1920%2C1080&ssl=1",
    },
    {
      property: "twitter:url",
      content: "https://portfolio-template.atalek.com/",
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
