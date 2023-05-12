<script setup>
  // Props
  defineProps({
    product: Object,
  })
</script>

<template>
  <section class="group product w-250 mb-8">
    <div class="relative">
      <img class="w-full" :src="product.image" :alt="product.name">
      <div class="z-50 flex items-center justify-center absolute bottom-0 bg-white/70 w-full h-24 translate-y-16 opacity-0 group-hover:translate-y-0 group-hover:opacity-100 transition-all duration-500">
        <div class="absolute flex gap-x-4 z-10">
          <img class="icon p-3 w-10 h-10 bg-custom-blue/80 hover:bg-custom-blue duration-350 transition-all" src="https://img.icons8.com/ios/50/ffffff/search--v1.png" alt="search">
          <img class="icon p-3 w-10 h-10 bg-custom-blue/80 hover:bg-custom-blue duration-350 transition-all" src="https://img.icons8.com/material-outlined/24/ffffff/shopping-cart--v1.png" alt="shopping-cart">
          <img class="icon p-3 w-10 h-10 bg-custom-blue/80 hover:bg-custom-blue duration-350 transition-all" src="https://img.icons8.com/ios/50/ffffff/hearts--v1.png" alt="favourite"/>
        </div>
      </div>
    </div>

    <div class="flex flex-col items-center justify-center py-4">
      <p class="capitalize text-custom-btn-gray">{{ product.category }}</p>
      <h3 class="group-hover:text-custom-blue transition-all duration-350 capitalize font-bold my-2">{{ product.name }}</h3>
      <span class="capitalize text-custom-btn-gray">${{ product.price }}.00</span>
    </div>
  </section>
</template>

<style scoped>
  .icon {
    cursor: pointer;
  }
</style>
