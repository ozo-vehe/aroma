<script setup>
  import heroBanner from '../assets/images/hero-banner.webp';
</script>

<template>
  <main class="min-h-screen flex flex-wrap bg-custom-background items-center justify-between gap-x-8 gap-y-4">
    <div class="relative w-450 h-screen bg-custom-blue">
      <img class="absolute left-24 bottom-0 w-450 h-600" :src="heroBanner" alt="Hero Banner">
    </div>

    <div class="w-650 heroText">
      <h4 class="text-3xl pb-4 text-gray-500">Shop is fun</h4>
      <h1 class="text-5xl uppercase font-bold pb-4">browse our premium product</h1>
      <p class="text-gray-700">
        Us which over of signs divide dominion deep fill bring 
        they're meat beho upon own earth without morning over third. 
        Their male dry. They are great appear whose land fly grass
      </p>
      <button class="bg-custom-blue text-white rounded-full transition-all duration-500 px-12 py-4 mt-12"> Browse Now</button>
    </div>
  </main>
</template>

<style scoped>
  .heroText {
    padding-right: 10%;
  }
</style>
