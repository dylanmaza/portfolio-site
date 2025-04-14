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
      <h1 class="font-extrabold text-5xl mb-6">
        Hi, ik ben <span class="text-green-600">Dylan Maza</span>, Frontend
        Developer
      </h1>
      <p class="mb-6">
        I'm a passionate frontend developer dedicated to creating beautiful and
        functional web experiences. Explore my work and see how I can bring your
        ideas to life.
      </p>
      <div class="inline-flex flex-wrap gap-4">
        <NuxtLink to="#projecten">
          <ButtonPri>Bekijk mijn werk</ButtonPri>
        </NuxtLink>
        <NuxtLink to="#contact">
          <ButtonSec>Contact</ButtonSec>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
