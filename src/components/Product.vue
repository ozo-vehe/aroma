<script setup>
  // Props
  defineProps({
    product: Object,
  })
</script>

<template>
  <section class="group product border border-black w-250">
    <div class="relative border border-green-400 overflow-hidden">
      <img class="w-full" :src="product.image" :alt="product.name">
      <div class="absolute bottom-0 z-10 bg-white/90 w-full h-32 translate-y-16 opacity-0 group-hover:translate-y-8 group-hover:opacity-100 transition-all duration-500">
        <div class="absolute flex gap-x-2 left-0 z-10">
          <img class="icon p-2 w-8 h-8 bg-custom-blue/80 hover:bg-custom-blue duration-350 transition-all rounded" src="https://img.icons8.com/ios/50/null/search--v1.png" alt="search">
          <img class="icon p-2 w-8 h-8 bg-custom-blue/80 hover:bg-custom-blue duration-350 transition-all rounded" src="https://img.icons8.com/material-outlined/24/null/shopping-cart--v1.png" alt="shopping-cart">
          <img class="icon p-2 w-8 h-8 bg-custom-blue/80 hover:bg-custom-blue duration-350 transition-all rounded" src="https://img.icons8.com/ios/50/null/hearts--v1.png" alt="favourite"/>
        </div>
      </div>
    </div>

    <div>
      <p>{{ product.category }}</p>
      <h3>{{ product.name }}</h3>
      <span>${{ product.price }}.00</span>
    </div>
  </section>
</template>

<style scoped>
  .icon {
    cursor: pointer;
  }
</style>
