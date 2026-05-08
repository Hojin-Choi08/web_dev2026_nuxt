<template>
  <div>
    <UContainer>
      <UPageHeader
        title="Portfolio"
        description="A selection of projects I've worked on."
      />
    </UContainer>

    <UPageSection title="Project Gallery">
      <UCarousel
        v-slot="{ item }"
        :items="items"
        :ui="{ item: 'basis-1/2 md:basis-1/3' }"
        arrows
        dots
      >
        <img
          :src="item"
          width="468"
          height="468"
          class="rounded-xl object-cover w-full h-56 px-2"
          loading="lazy"
        />
      </UCarousel>
    </UPageSection>
  </div>
</template>

<script setup>
const items = [
  "https://picsum.photos/468/468?random=1",
  "https://picsum.photos/468/468?random=2",
  "https://picsum.photos/468/468?random=3",
  "https://picsum.photos/468/468?random=4",
  "https://picsum.photos/468/468?random=5",
  "https://picsum.photos/468/468?random=6",
];
</script>
