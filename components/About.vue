<script setup lang="ts">
const skills = [
  'HTML',
  'CSS',
  'Javascript',
  'Typescript',
  'Vue',
  'Nuxt',
  'GSAP',
  'Tailwind',
];
</script>

<template>
  <div class="text-center px-4 my-25">
    <div class="max-w-2xl mx-auto">
      <h2 class="font-extrabold text-4xl mb-5">Over mij</h2>
      <p class="mb-5">
        Kort stukje over jezelf als persoon (hobby’s, interesses, karakter) én
        je ervaring/skills als frontend developer.
      </p>
      <ul class="flex flex-wrap gap-4">
        <li
          v-for="(skill, index) in skills"
          :key="index"
          v-text="skill"
          class="py-2 px-3 bg-black text-white rounded"
        />
      </ul>
    </div>
  </div>
</template>
