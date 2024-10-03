<template>
  <header class="bg-white shadow-md">
    <div class="px-4 mx-auto sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16 lg:h-20">
        <div class="flex-shrink-0">
          <a href="/" title="" class="flex">
            <img class="w-auto h-16" :src="logoSrc" alt="Logo" />
          </a>
        </div>

        <div class="hidden md:flex flex-grow items-center justify-center">
          <nav class="space-x-8">
            <a
              v-for="item in navItems"
              :key="item.href"
              :href="item.href"
              class="text-lg font-semibold text-gray-800 transition-all duration-200 hover:text-blue-600"
            >
              {{ item.text }}
            </a>
          </nav>
        </div>

        <div class="md:hidden">
          <button @click="toggleMenu" class="text-gray-800 hover:text-blue-600">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile menu -->
    <div v-if="isMenuOpen" class="md:hidden">
      <nav class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
        <a
          v-for="item in navItems"
          :key="item.href"
          :href="item.href"
          class="block px-3 py-2 rounded-md text-base font-medium text-gray-800 hover:text-blue-600 hover:bg-gray-50"
          @click="closeMenu"
        >
          {{ item.text }}
        </a>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';

defineProps({
  logoSrc: String,
  companyName: String,
  navItems: Array,
});

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const closeMenu = () => {
  isMenuOpen.value = false;
};
</script>
