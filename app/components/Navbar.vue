<template>
  <UHeader title="I LOVE WONHEE">
    <UNavigationMenu :items="items" />
    <template #right>
      <UColorModeButton />
      <button
        class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600"
      >
        Sign In
      </button>
    </template>
  </UHeader>
</template>
<script setup>
const items = [
  {
    label: "Item 1",
    to: "/",
    children: [{ label: "Sub Item 1", to: "/" }],
  },
  { label: "Item 2", to: "/", children: [{ label: "Sub Item 2", to: "/" }] },
  { label: "Item 3", to: "/", children: [{ label: "Sub Item 3", to: "/" }] },
];
</script>
