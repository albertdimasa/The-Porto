<template>
  <div class="py-12 bg-gray-50 min-h-screen">
    <div class="container mx-auto px-4 max-w-4xl">
      <h1 class="text-4xl font-bold text-center mb-12">My Blog</h1>
      <div class="space-y-8">
        <BlogCard v-for="post in posts" :key="post._path" :project="post" />
      </div>
    </div>
  </div>
</template>

<script setup>
const { data: posts } = await useAsyncData('blog', () => queryCollection('blog').limit(3).all())

// const { data: posts } = await queryContent('blog').all()
// console.log("blog: ", posts.value)
</script>
