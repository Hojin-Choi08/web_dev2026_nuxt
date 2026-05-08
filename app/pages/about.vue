<template>
  <div>
    <UContainer>
      <UPageHeader
        title="About Me"
        description="Learn more about who I am and what I do."
      />
    </UContainer>

    <UPageBody>
      <UPageSection title="Who Am I?">
        <div class="flex flex-col md:flex-row items-center gap-8">
          <img
            src="https://picsum.photos/200/200?random=99"
            class="rounded-full w-40 h-40 object-cover shadow-lg"
            alt="Profile photo"
          />
          <p class="text-gray-500">
            I'm a front-end developer passionate about creating beautiful,
            user-friendly web applications using modern tools like Vue, Nuxt,
            and Tailwind CSS.
          </p>
        </div>
      </UPageSection>
    </UPageBody>
  </div>
</template>
