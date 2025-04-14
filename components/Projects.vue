<script setup lang="ts">
const projects = [
  {
    title: 'Action jobs',
    url: 'https://nl.action.jobs',
    logo: '/action.png',
  },
  {
    title: 'Landal jobs',
    url: 'https://jobs.landal.com',
    logo: '/landal.png',
  },
  {
    title: 'Werken bij het CAK',
    url: 'https://werkenbijhetcak.nl',
    logo: '/cak.png',
  },
  {
    title: 'Maak werk van een schonere wereld',
    url: 'https://www.maakwerkvaneenschonerewereld.nl',
    logo: '/mwsw.png',
  },
  {
    title: 'Veva',
    url: 'https://veva.nl',
    logo: '/veva.png',
  },
  {
    title: 'Werken bij De Belastingdienst',
    url: 'https://werken.belastingdienst.nl',
    logo: '/belastingdienst.svg',
  },
  {
    title: 'Werken bij DNB',
    url: 'https://www.werkenbijdnb.nl',
    logo: '/dnb.png',
  },
  {
    title: 'Werken bij het Loodswezen',
    url: 'https://werkenbijhetloodswezen.nl/',
    logo: '/hetloodswezen.png',
  },
];
</script>

<template>
  <div class="my-25 text-center">
    <div class="px-4 mb-5">
      <div class="max-w-4xl mx-auto">
        <h2 class="font-extrabold text-4xl mb-10">Meer werk</h2>
        <ul class="grid md:grid-cols-3 gap-5">
          <li v-for="(project, index) in projects" :key="index">
            <NuxtLink
              :to="project.url"
              target="_blank"
              class="grid h-full p-5 border-2 gap-3 rounded"
            >
              <img
                v-if="project.logo"
                :src="project.logo"
                alt=""
                class="size-12 rounded-full mx-auto"
                width="48"
                height="48"
                loading="lazy"
              />
              <h2 v-text="project.title" class="font-extrabold text-2xl" />
            </NuxtLink>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
