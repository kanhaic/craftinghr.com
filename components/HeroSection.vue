<template>
  <div class="">
    <section class="bg-[#FCF8F1] bg-opacity-30 dark:bg-gray-900 py-10 sm:py-16 lg:py-24">
      <div class="px-4 mx-auto max-w-7xl sm:px-6 lg:px-8">
        <div class="grid items-center grid-cols-1 gap-12 lg:grid-cols-2">
          <div>
            <p
              class="text-base font-semibold tracking-wider text-blue-600 uppercase dark:text-blue-400"
            >
              {{ preTitle }}
            </p>
            <h1
              class="mt-4 text-4xl font-bold text-black lg:mt-8 sm:text-6xl xl:text-6xl dark:text-white"
            >
              {{ title }}
            </h1>
            <p class="mt-4 text-base text-black lg:mt-8 sm:text-xl dark:text-white">
              {{ subtitle }}
            </p>

            <a
              href="#products"
              title=""
              class="inline-flex items-center px-6 py-4 mt-8 font-semibold text-black transition-all duration-200 bg-yellow-300 rounded-full lg:mt-16 hover:bg-yellow-400 focus:bg-yellow-400 dark:text-black"
              role="button"
            >
              Learn More
              <svg
                class="w-6 h-6 ml-8 -mr-2 dark:text-black"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="1.5"
                  d="M13 9l3 3m0 0l-3 3m3-3H8m13 0a9 9 0 11-18 0 9 9 0 0118 0z"
                />
              </svg>
            </a>
          </div>

          <div>
            <img
              class="w-full rounded-lg shadow-lg border-2 border-gray-200 dark:border-gray-800"
              src="https://images.unsplash.com/photo-1520607162513-77705c0f0d4a?q=80&w=3538&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
              alt="Hero Image"
            />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
defineProps({
  preTitle: String,
  title: String,
  subtitle: String,
  ctaText: String,
});
</script>