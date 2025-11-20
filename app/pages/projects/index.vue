<template>
  <div class="py-12 bg-gray-50 min-h-screen">
    <div class="container mx-auto px-4">
      <h1 class="text-4xl font-bold text-center mb-12">My Projects</h1>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <ProjectCard v-for="project in projects" :key="project._path" :project="project" />
      </div>
    </div>
  </div>
</template>

<script setup>
const { data: projects } = await useAsyncData('projects', () => queryCollection('projects').all())
console.log('Projects data:', projects.value)
</script>
