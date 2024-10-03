<template>
  <div class="bg-white py-12 sm:py-16 mx-auto">
    <section id="products" class="py-20">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12">{{ title }}</h2>
        <div class="grid md:grid-cols-2 gap-12">
          <ProductCard
            v-for="product in products"
            :key="product.title"
            :title="product.title"
            :description="product.description"
            :link="product.link"
            :logo="product.logo"
          />
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>

defineProps({
  title: String,
  products: Array,
});
</script>
