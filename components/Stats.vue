<template>
  <div class="bg-gray-900 py-12 sm:py-16 dark:bg-gray-900 border-b border-gray-800 ">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:max-w-none">
        <div class="text-center">
          <h2 class="text-3xl font-bold tracking-tight dark:text-white sm:text-4xl">{{ title }}</h2>
          <p class="mt-4 text-lg leading-8 text-gray-300 dark:text-gray-500">{{ subtitle }}</p>
        </div>
        <dl class="mt-16 grid grid-cols-1 gap-0.5 overflow-hidden rounded-2xl text-center sm:grid-cols-3 lg:grid-cols-3">
          <div v-for="stat in stats" :key="stat.id" class="flex flex-col bg-white/5 p-8">
              <dt class="text-sm font-semibold leading-6 text-gray-300">{{ stat.name }}</dt>
              <dd class="order-first text-3xl font-semibold tracking-tight text-white">{{ stat.value }}</dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  subtitle: {
    type: String,
    required: true,
  },
  stats: {
    type: Array,
    required: true,
  },
});
</script>