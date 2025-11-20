<template>
  <div class="py-12 bg-white min-h-screen">
    <div class="container mx-auto px-4 max-w-3xl">
      <NuxtLink to="/blog" class="text-indigo-600 hover:underline mb-6 inline-block">&larr; Back to Blog</NuxtLink>
      <ContentDoc v-slot="{ doc }">
        <article class="prose lg:prose-xl mx-auto">
          <h1 class="text-4xl font-bold mb-2">{{ doc.title }}</h1>
          <div class="text-gray-500 mb-8">{{ doc.date }}</div>
          <img v-if="doc.image" :src="doc.image" :alt="doc.title" class="w-full h-64 object-cover rounded-lg mb-8 shadow-md">
          <ContentRenderer :value="doc" />
        </article>
      </ContentDoc>
    </div>
  </div>
</template>
