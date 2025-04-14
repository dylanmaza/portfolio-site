<script setup lang="ts">
const featuredProjects = [
  {
    title: 'Werken bij defensie',
    description:
      'Het officiële wervingsplatform van Defensie. De site biedt informatie over militaire en burgerfuncties, opleidingen en carrièremogelijkheden. Met tools zoals een beroepenzoeker helpt het bezoekers bij het vinden van een passende rol binnen Defensie.',
    url: 'https://werkenbijdefensie.nl',
    videoUrl: '/werkenbijdefensie-nl-home-praktische-info.mp4',
    imageUrl: null,
    tags: ['Laravel', 'Vue 2', 'jQuery', 'GSAP', 'Tailwind'],
  },
  {
    title: 'Werken bij Dienst Toeslagen',
    description:
      'Bijna 6 miljoen huishoudens in Nederland krijgen maandelijks een toeslag die voor hen onmisbaar is om de kosten te betalen van de huur, de zorgverzekering, de zorg voor kinderen en de kinderopvang.',
    url: 'https://werkenbij.diensttoeslagen.nl',
    videoUrl: null,
    imageUrl: '/werkenbij-diensttoeslagen-nl-home.png',
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
  <div id="projecten" class="py-25 text-center bg-gray-50">
    <div class="px-4 mb-5">
      <div class="max-w-2xl mx-auto">
        <h2 class="font-extrabold text-4xl mb-10">Uitgelicht werk</h2>
      </div>
    </div>
    <div class="max-w-7xl mx-auto">
      <div class="grid gap-20 text-left">
        <div v-for="(project, index) in featuredProjects" :key="index">
          <video
            v-if="project.videoUrl"
            :src="project.videoUrl"
            width="1280"
            height="654"
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
