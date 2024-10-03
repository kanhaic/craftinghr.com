<template>
  <div class="bg-white dark:bg-gray-900 py-20">
    <section id="contact" class="container mx-auto px-4 text-center">
      <h2 class="text-3xl font-bold mb-8 dark:text-white">{{ title }}</h2>
        <p class="text-xl mb-8 dark:text-gray-400">{{ subtitle }}</p>
        <a
          :href="'mailto:' + email"
          class="bg-blue-600 text-white px-6 py-3 rounded-lg font-semibold hover:bg-blue-700 transition duration-300 dark:bg-blue-400 dark:text-white dark:hover:bg-blue-500 dark:hover:text-white  "
        >
          {{ ctaText }}
        </a>
    </section>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  subtitle: String,
  ctaText: String,
  email: String,
});
</script>