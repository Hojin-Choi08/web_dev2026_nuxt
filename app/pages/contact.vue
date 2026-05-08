<template>
  <div>
    <UContainer>
      <UPageHeader
        title="Contact"
        description="Have a question or want to work together?"
      />
    </UContainer>

    <UPageSection title="Send a Message">
      <UCard class="max-w-lg mx-auto">
        <UForm @submit="processForm">
          <div class="flex flex-col gap-4">
            <UFormField label="First Name" required>
              <UInput v-model="firstName" placeholder="John" class="w-full" />
            </UFormField>
            <UFormField label="Last Name" required>
              <UInput v-model="lastName" placeholder="Doe" class="w-full" />
            </UFormField>
            <UFormField label="Email" required>
              <UInput
                v-model="email"
                type="email"
                placeholder="john@example.com"
                class="w-full"
              />
            </UFormField>
            <UFormField label="Message" required>
              <UTextarea
                v-model="message"
                placeholder="Write your message here..."
                class="w-full"
              />
            </UFormField>
            <UButton type="submit" class="w-full justify-center"
              >Send Message</UButton
            >
          </div>
        </UForm>
        <div
          v-if="submitted"
          class="mt-4 p-4 rounded-lg bg-green-50 text-green-700 text-center"
        >
          ✅ Thanks, {{ submittedName }}! We'll be in touch.
        </div>
      </UCard>
    </UPageSection>

    <UPageSection title="Frequently Asked Questions">
      <UAccordion :items="faqs" class="max-w-2xl mx-auto" />
    </UPageSection>
  </div>
</template>

<script setup>
const firstName = ref("");
const lastName = ref("");
const email = ref("");
const message = ref("");
const submittedName = ref("");
const submitted = ref(false);

function processForm() {
  submittedName.value = `${firstName.value} ${lastName.value}`;
  submitted.value = true;
  firstName.value = "";
  lastName.value = "";
  email.value = "";
  message.value = "";
}

const faqs = [
  {
    label: "How long does a project take?",
    content:
      "Most projects take between 2–6 weeks depending on scope and complexity.",
  },
  {
    label: "Do you work remotely?",
    content: "Yes! I work fully remote and collaborate with clients worldwide.",
  },
  {
    label: "What's your preferred tech stack?",
    content:
      "I love working with Vue, Nuxt, and Tailwind CSS for modern web projects.",
  },
];
</script>
