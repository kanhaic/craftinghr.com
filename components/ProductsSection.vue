<template>
  <div class="bg-white py-12 sm:py-16 dark:bg-gray-900  border-gray-800 dark:border-gray-200">
    <div class="mx-auto max-w-6xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:text-center">
        <h2 class="text-base font-semibold leading-7 text-indigo-600 dark:text-blue-400">{{ preTitle }}</h2>
        <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl dark:text-white">{{ title }}</p>
        <p class="mt-6 text-lg leading-8 text-gray-600 dark:text-gray-400">{{ subtitle }}</p>
      </div>
      <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-none">
        <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-16 lg:max-w-none lg:grid-cols-2">
          <div v-for="product in products" :key="product.name" class="relative">
            <div class="absolute -inset-2">
              <div class="w-full h-full mx-auto opacity-30 blur-lg filter" style="background: linear-gradient(90deg, #44ff9a -0.55%, #44b0ff 22.86%, #8b44ff 48.36%, #ff6644 73.33%, #ebff70 99.34%)"></div>
            </div>
            <div class="relative flex flex-col bg-white py-6 px-6 rounded-lg shadow-md dark:bg-gray-800">
              <dt class="flex items-center gap-x-3 text-base font-semibold leading-7 text-gray-900 dark:text-white">
                <img :src="product.logo" :alt="product.name" class="h-8 w-8" />
                {{ product.name }}
              </dt>
              <dd class="mt-4 flex flex-auto flex-col text-base leading-7 text-gray-600 dark:text-gray-400">
                <p class="flex-auto">{{ product.description }}</p>
                <p class="mt-6">
                  <a :href="product.href" class="text-sm font-semibold leading-6 text-indigo-600 dark:text-blue-400">Learn more <span aria-hidden="true">→</span></a>
                </p>
              </dd>
            </div>
          </div>
        </dl>
      </div>
    </div>
    <div class="mt-24 bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500 h-1 w-1/3 mx-auto"></div>
  </div>
</template>

<script setup>

  defineProps({
    preTitle: String,
    title: String,
    subtitle: String,
    products: Array
  });
  
</script>