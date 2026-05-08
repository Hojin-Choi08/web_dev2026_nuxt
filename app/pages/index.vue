<template>
  <div>
    <UPageHero
      title="Welcome to My Portfolio"
      description="I'm a creative developer building modern, accessible web experiences with Vue & Nuxt."
      :links="links"
    />

    <UPageSection
      title="What I Do"
      description="Here's a quick overview of my skills and services."
    >
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <UCard v-for="skill in skills" :key="skill.title">
          <div class="text-3xl mb-2">{{ skill.icon }}</div>
          <h3 class="font-semibold mb-1">{{ skill.title }}</h3>
          <p class="text-gray-500 text-sm">{{ skill.description }}</p>
        </UCard>
      </div>
    </UPageSection>

    <UPageCTA
      title="Interested in working together?"
      description="Let's build something great. Reach out and let's talk."
      :links="[{ label: 'Contact Me', to: '/contact', color: 'primary' }]"
    />
  </div>
</template>

<script setup>
const links = [
  { label: "View Portfolio", to: "/portfolio", color: "primary" },
  { label: "Contact Me", to: "/contact", variant: "outline" },
];

const skills = [
  {
    icon: "🎨",
    title: "Design",
    description: "Clean, modern UI with custom Tailwind themes.",
  },
  {
    icon: "⚡",
    title: "Performance",
    description: "Blazing fast pages powered by Nuxt 3.",
  },
  {
    icon: "♿",
    title: "Accessibility",
    description: "Built with accessibility best practices in mind.",
  },
];
</script>
