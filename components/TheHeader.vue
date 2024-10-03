<template>
  <header class="bg-white shadow-md">
    <div class="px-4 mx-auto sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16 lg:h-20">
        <div class="flex-shrink-0">
          <a href="/" title="" class="flex">
            <img class="w-auto h-16" :src="logoSrc" alt="Logo" />
          </a>
        </div>

        <div class="flex-grow flex items-center justify-center">
          <nav class="space-x-8">
            <a
              v-for="item in navItems"
              :key="item.href"
              :href="item.href"
              class="text-lg font-semibold text-gray-800 transition-all duration-200 hover:text-blue-600 "
            >
              {{ item.text }}
            </a>
          </nav>
        </div>

        <div class="flex-shrink-0 w-16">
          <!-- This empty div balances the layout -->
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
defineProps({
  logoSrc: String,
  companyName: String,
  navItems: Array,
});
</script>
