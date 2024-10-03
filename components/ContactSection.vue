<template>
  <section id="contact" class="bg-gray-200 py-20">
    <div class="container mx-auto px-4 text-center">
      <h2 class="text-3xl font-bold mb-8">{{ title }}</h2>
      <p class="text-xl mb-8">{{ subtitle }}</p>
      <a :href="'mailto:' + email" class="bg-blue-600 text-white px-6 py-3 rounded-lg font-semibold hover:bg-blue-700 transition duration-300">
        {{ ctaText }}
      </a>
    </div>
  </section>
</template>

<script setup>
defineProps({
  title: String,
  subtitle: String,
  ctaText: String,
  email: String,
})
</script>