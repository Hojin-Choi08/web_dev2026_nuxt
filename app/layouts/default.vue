<template>
  <UApp>
    <UHeader>
      <template #left>
        <NuxtLink to="/" class="font-bold text-xl">My Portfolio</NuxtLink>
      </template>
      <UNavigationMenu :items="navItems" />
    </UHeader>

    <main>
      <slot />
    </main>

    <UFooter>
      <template #left>
        <p class="text-sm text-gray-500">
          © 2026 My Portfolio. All rights reserved.
        </p>
      </template>
    </UFooter>
  </UApp>
</template>

<script setup>
const navItems = [
  { label: "Home", to: "/" },
  { label: "About", to: "/about" },
  { label: "Portfolio", to: "/portfolio" },
  { label: "Contact", to: "/contact" },
];
</script>
