<template>
  <div class="bg-white rounded-lg shadow-lg overflow-hidden hover:shadow-xl transition duration-300">
    <img :src="project.image" :alt="project.title" class="w-full h-48 object-cover">
    <div class="p-6">
      <h3 class="text-xl font-semibold mb-2">{{ project.title }}</h3>
      <p class="text-gray-600 mb-4 line-clamp-2">{{ project.description }}</p>
      <div class="flex flex-wrap gap-2 mb-4">
        <span v-for="tag in project.tags" :key="tag" class="bg-indigo-100 text-indigo-800 text-xs px-2 py-1 rounded-full">
          {{ tag }}
        </span>
      </div>
      <NuxtLink :to="project._path" class="inline-block bg-indigo-600 text-white px-4 py-2 rounded hover:bg-indigo-700 transition">
        View Details
      </NuxtLink>
    </div>
  </div>
</template>

<script setup>
defineProps({
  project: {
    type: Object,
    required: true
  }
})
</script>
