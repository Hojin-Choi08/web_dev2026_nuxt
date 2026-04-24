<template>
  <div>
    <UPageHero
      title="Ultimate Vue UI library"
      description="A Nuxt/Vue-integrated UI library providing a rich set of fully-styled, accessible and highly customizable components for building modern web applications."
      :links="links"
    />
  </div>
</template>
<script setup>
const links = [
  {
    label: "Get Started",
    to: "/docs",
    variant: "outline",
  },
  {
    label: "GitHub",
    to: "https://github.com/nuxt/ui",
    variant: "outline",
  },
];
</script>
