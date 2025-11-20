<template>
  <div class="bg-white rounded-lg shadow-md p-6 hover:shadow-lg transition duration-300 border-l-4 border-indigo-500">
    <div class="text-sm text-gray-500 mb-2">{{ project.date }}</div>
    <h3 class="text-xl font-bold mb-2">
      <NuxtLink :to="project._path" class="hover:text-indigo-600 transition">{{ project.title }}</NuxtLink>
    </h3>
    <p class="text-gray-600 mb-4 line-clamp-3">{{ project.description }}</p>
    <NuxtLink :to="project._path" class="text-indigo-600 font-medium hover:underline">
      Read more &rarr;
    </NuxtLink>
  </div>
</template>

<script setup>
defineProps({
  project: { // Using 'project' prop name to match generic usage or rename to 'post'
    type: Object,
    required: true
  }
})
</script>
