<template>
  <div class="text-center px-4 mb-25 mt-10 md:mt-25">
    <div class="max-w-2xl mx-auto">
      <img
        src="/public/dylan.jpg"
        width="200"
        height="200"
        class="mb-6 size-50 rounded-full mx-auto"
        alt=""
      />
      <h1 class="font-bold text-5xl mb-6">
        Hi, ik ben Dylan Maza, Frontend Developer
      </h1>
      <p class="mb-6">
        I'm a passionate frontend developer dedicated to creating beautiful and
        functional web experiences. Explore my work and see how I can bring your
        ideas to life.
      </p>
      <div class="inline-flex flex-wrap gap-4">
        <NuxtLink to="#projecten" class="py-3 px-5 bg-black text-white">
          Bekijk mijn werk
        </NuxtLink>
        <NuxtLink to="#contact" class="py-3 px-5 border">Contact</NuxtLink>
      </div>
    </div>
  </div>
</template>
