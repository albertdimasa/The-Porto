<template>
  <div>
    <!-- Hero Section -->
    <section class="bg-indigo-700 text-white py-20">
      <div class="container mx-auto px-4 text-center">
        <h1 class="text-4xl md:text-6xl font-bold mb-4">Hi, I'm [Your Name]</h1>
        <p class="text-xl md:text-2xl mb-8 text-indigo-100">Full Stack Developer & UI/UX Enthusiast</p>
        <NuxtLink to="/projects" class="bg-white text-indigo-700 font-bold py-3 px-8 rounded-full hover:bg-indigo-50 transition duration-300">
          View My Work
        </NuxtLink>
      </div>
    </section>

    <!-- Featured Projects Preview -->
    <section class="py-16 bg-gray-50">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12">Featured Projects</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <ProjectCard v-for="project in projects" :key="project._path" :project="project" />
        </div>
        <div class="text-center mt-12">
          <NuxtLink to="/projects" class="text-indigo-600 font-semibold hover:text-indigo-800">
            See All Projects &rarr;
          </NuxtLink>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12">Skills & Technologies</h2>
        <div class="flex flex-wrap justify-center gap-4">
          <span class="px-6 py-3 bg-gray-100 rounded-lg text-gray-700 font-medium">Vue.js / Nuxt</span>
          <span class="px-6 py-3 bg-gray-100 rounded-lg text-gray-700 font-medium">React / Next.js</span>
          <span class="px-6 py-3 bg-gray-100 rounded-lg text-gray-700 font-medium">Tailwind CSS</span>
          <span class="px-6 py-3 bg-gray-100 rounded-lg text-gray-700 font-medium">Node.js</span>
          <span class="px-6 py-3 bg-gray-100 rounded-lg text-gray-700 font-medium">TypeScript</span>
          <span class="px-6 py-3 bg-gray-100 rounded-lg text-gray-700 font-medium">PostgreSQL</span>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const { data: projects } = await useAsyncData('projects', () => queryCollection('projects').limit(3).all())
</script>
