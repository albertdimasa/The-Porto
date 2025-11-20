<template>
  <nav class="bg-white shadow-md">
    <div class="container mx-auto px-4 py-4 flex justify-between items-center">
      <NuxtLink to="/" class="text-2xl font-bold text-indigo-600">MyPortfolio</NuxtLink>
      <div class="hidden md:flex space-x-6">
        <NuxtLink to="/" class="text-gray-700 hover:text-indigo-600 transition">Home</NuxtLink>
        <NuxtLink to="/projects" class="text-gray-700 hover:text-indigo-600 transition">Projects</NuxtLink>
        <NuxtLink to="/blog" class="text-gray-700 hover:text-indigo-600 transition">Blog</NuxtLink>
      </div>
      <!-- Mobile Menu Button (Simplified) -->
      <div class="md:hidden">
        <button class="text-gray-700 focus:outline-none">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
          </svg>
        </button>
      </div>
    </div>
  </nav>
</template>
