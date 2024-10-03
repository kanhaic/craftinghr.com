<template>
  <div class="bg-white dark:bg-gray-900">
    <div class="mx-auto max-w-7xl px-6 lg:px-8 py-12 sm:py-16 lg:py-20">
      <div class="text-center mb-16">
        <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl dark:text-white">{{ title }}</h2>
        <p class="mt-4 text-lg leading-8 text-gray-600 dark:text-gray-400">{{ subtitle }}</p>
      </div>
      <div class="grid grid-cols-1 gap-12 lg:grid-cols-2">
        <div v-for="member in teamMembers" :key="member.name" class="flex flex-col items-center sm:flex-row sm:items-start">
          <div class="w-full sm:w-48 flex justify-center sm:justify-start sm:flex-shrink-0">
            <img class="object-cover w-48 h-48 rounded-2xl -rotate-3" :src="member.image" :alt="member.name" />
          </div>
          <div class="mt-8 sm:mt-0 sm:ml-10">
          <div class="mt-8 sm:mt-0 sm:ml-10 text-center sm:text-left">
            <p class="text-4xl font-semibold tracking-tight text-gray-900 dark:text-white">{{ member.name }}</p>
            <p class="mt-3 text-xs font-semibold tracking-widest text-gray-900 uppercase dark:text-gray-400">{{ member.title }}</p>
            <p class="mt-8 text-base font-normal text-gray-600 dark:text-gray-400">{{ member.description }}</p>
            <div class="mt-8">
              <a :href="member.linkedIn" target="_blank" rel="noopener noreferrer" class="inline-flex items-center text-sm font-semibold text-blue-600 transition-all duration-200 group hover:text-blue-800 hover:underline dark:text-blue-400">
                Follow on LinkedIn
                <svg class="w-5 h-5 ml-1 group-hover:translate-x-0.5 group-hover:-translate-y-0.5 transition-all duration-200" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5" fill="none" stroke-linecap="round" stroke-linejoin="round">
                  <line x1="7" y1="17" x2="17" y2="7"></line>
                  <polyline points="7 7 17 7 17 17"></polyline>
                </svg>
              </a>
            </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Rainbow border -->
    <div class="mt-24 bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500 h-1 w-1/3 mx-auto"></div>
  </div>

</template>
<script setup>
defineProps({
  title: String,
  subtitle: String,
  teamMembers: Array,
})
</script>