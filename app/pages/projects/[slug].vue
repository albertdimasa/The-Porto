<template>
  <div class="py-12 bg-white min-h-screen">
    <div class="container mx-auto px-4 max-w-4xl">
      <NuxtLink to="/projects" class="text-indigo-600 hover:underline mb-6 inline-block">&larr; Back to Projects</NuxtLink>
      <ContentDoc v-slot="{ doc }">
        <article class="prose lg:prose-xl mx-auto">
          <img :src="doc.image" :alt="doc.title" class="w-full h-64 object-cover rounded-lg mb-8 shadow-md">
          <h1 class="text-4xl font-bold mb-4">{{ doc.title }}</h1>
          <div class="flex gap-2 mb-8">
            <span v-for="tag in doc.tags" :key="tag" class="bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">
              {{ tag }}
            </span>
          </div>
          <ContentRenderer :value="doc" />
        </article>
      </ContentDoc>
    </div>
  </div>
</template>
