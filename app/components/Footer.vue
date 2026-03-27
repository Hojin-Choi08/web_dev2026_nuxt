<template>
  <UFooter>
    <UNavigationMenu :items="items" />
    <template #right>
      <span class="text-gray-500">Illit</span>
    </template>
  </UFooter>
</template>
<script setup>
const items = [
  { label: "Item 1", to: "/" },
  { label: "Item 2", to: "/" },
  { label: "Item 3", to: "/" },
];
</script>
