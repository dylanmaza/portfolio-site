<script setup type="ts">
import { IconLinkedIn, IconGithub, IconMail } from '#components';
const socials = [
  {
    url: 'https://www.linkedin.com/in/dylan-maza',
    icon: IconLinkedIn,
    text: 'Bezoek mijn LinkedIn pagina',
  },
  {
    url: 'https://github.com/dylanmaza',
    icon: IconGithub,
    text: 'Bezoek mijn GitHub pagina',
  },
  {
    url: 'mailto:dylanmaza2@gmail.com',
    icon: IconMail,
    text: 'Stuur mij een e-mail',
  },
];
</script>

<template>
  <div id="contact" class="text-center px-4 my-25">
    <div class="max-w-2xl mx-auto">
      <h2 class="font-bold text-4xl mb-5">Contact</h2>
      <ul class="inline-flex flex-wrap gap-3">
        <li v-for="(social, index) in socials" :key="index">
          <NuxtLink :to="social.url" :title="social.text" target="_blank">
            <component :is="social.icon" class="size-10" />
            <span v-text="social.text" class="sr-only" />
          </NuxtLink>
        </li>
      </ul>
    </div>
  </div>
</template>
