<template>
  <footer class="bg-gray-800 text-white py-6">
    <div class="container mx-auto px-4 text-center">
      <p>&copy; {{ currentYear }} {{ companyName }}. All rights reserved.</p>
    </div>
  </footer>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  companyName: String,
})

const currentYear = computed(() => new Date().getFullYear())
</script>