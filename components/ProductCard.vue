<template>
  <div class="bg-white rounded-lg shadow-md overflow-hidden transition-all duration-300 hover:shadow-xl hover:scale-105">
    <div class="p-6 bg-gradient-to-br from-blue-500 to-purple-600">
      <img :src="logo" :alt="title + ' logo'" class="w-16 h-16 mb-4 mx-auto">
      <h3 class="text-2xl font-semibold mb-2 text-white">{{ title }}</h3>
    </div>
    <div class="p-6">
      <p class="text-gray-600 mb-4">{{ description }}</p>
      <a :href="link" target="_blank" class="inline-block bg-blue-600 text-white px-4 py-2 rounded-full font-semibold hover:bg-blue-700 transition duration-300">
        Learn More
      </a>
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  link: String,
  logo: String,
})
</script>