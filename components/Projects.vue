<script setup lang="ts">
const projects = [
  {
    title: 'Werkenbijdefensie',
    description:
      'Het officiële wervingsplatform van Defensie. De site biedt informatie over militaire en burgerfuncties, opleidingen en carrièremogelijkheden. Met tools zoals een beroepenzoeker helpt het bezoekers bij het vinden van een passende rol binnen Defensie.',
    url: 'https://werkenbijdefensie.nl',
    videoUrl: '/werkenbijdefensie-nl-home-praktische-info.mp4',
    imageUrl: null,
    tags: ['Laravel', 'Vue 2', 'jQuery', 'GSAP', 'Tailwind'],
  },
  {
    title: 'WerkenbijhetCAK',
    description:
      'Iedere burger heeft recht heeft op dienstverlening met de menselijke maat. Dat is onze norm. Hiermee bedoelen we dienstverlening op een manier die op dat moment bij de situatie van de burger past. Iedereen kan met het CAK te maken krijgen.',
    url: 'https://werkenbijhetcak.nl',
    videoUrl: null,
    imageUrl: '/werkenbijhetcak-nl-home.png',
    tags: [
      'Headless',
      'Nuxt 3',
      'Composition API',
      'Vue Transitions',
      'Tailwind',
      'Toegankelijkheid WCAG 2.1, Niveau AA',
    ],
  },
];
</script>

<template>
  <div id="mijn-werk" class="my-25 text-center">
    <div class="px-4 mb-5">
      <div class="max-w-7xl mx-auto">
        <h2 class="font-bold text-4xl mb-5">Projecten</h2>
        <p>Explore my diverse range of frontend development projects.</p>
      </div>
    </div>
    <div class="max-w-7xl mx-auto">
      <div class="grid gap-20 text-left">
        <div v-for="(project, index) in projects" :key="index">
          <video
            v-if="project.videoUrl"
            :src="project.videoUrl"
            controls
          ></video>
          <img
            v-else-if="project.imageUrl"
            :src="project.imageUrl"
            width="1280"
            height="720"
            alt=""
            class="aspect-video object-cover object-top"
            loading="lazy"
          />
          <div class="grid md:grid-cols-2 items-center gap-3 mt-4 px-4 md:px-0">
            <div>
              <h3 class="text-2xl font-bold mb-2">
                <NuxtLink
                  :to="project.url"
                  target="_blank"
                  external
                  class="inline-flex gap-1"
                >
                  {{ project.title }}
                  <IconExternalLink width="20" />
                </NuxtLink>
              </h3>
              <ul
                v-if="project.tags?.length"
                class="flex flex-wrap gap-x-3 gap-y-2"
              >
                <li
                  v-for="(tag, index) in project.tags"
                  :key="index"
                  v-text="tag"
                  class="py-1 px-2 bg-black text-white rounded"
                />
              </ul>
            </div>
            <p v-if="project.description" v-text="project.description" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
